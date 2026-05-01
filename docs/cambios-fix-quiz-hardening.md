# Cambios realizados en `codex/fix-quiz-hardening`

Fecha: 1 de mayo de 2026

## Objetivo

Reforzar la app sin cambiar su enfoque de producto: mismo flujo, menos errores, mejor accesibilidad y un consentimiento de cookies más correcto.

## Cambios funcionales

- Se evita responder varias veces la misma pregunta.
- Se bloquean las opciones justo después de la primera respuesta.
- Se mantiene el botón `Continuar` con una breve pausa para que el usuario vea el resultado.
- Se añade un contador visible de progreso: `Pregunta X de 10`.

## Manejo de errores

- Se añade control de errores al cargar `menu_temas.json`.
- Se añade control de errores al cargar cada cuestionario JSON.
- Se muestra un mensaje claro al usuario si falla la carga.
- Se añade botón de reintento para no dejar la app en un estado silencioso.

## Accesibilidad y UX

- Las respuestas dejan de ser `li` clicables y pasan a renderizarse como botones reales.
- Se mejora la navegación por teclado.
- El feedback ya no depende solo del color: ahora aparece texto visual de `Correcta` o `Incorrecta`.
- Se añade una región `aria-live` para anunciar el resultado de la respuesta.

## Cookies y analítica

- Google Analytics ya no se carga al entrar en la página.
- Analytics solo se inicializa si el usuario acepta cookies analíticas.
- Se sustituye el banner anterior por uno con dos opciones: aceptar o rechazar.
- La decisión se guarda en `localStorage`.

## Política de cookies

- Se fija una fecha de actualización real en lugar de mostrar siempre la fecha actual del navegador.
- Se aclara que las cookies analíticas solo se activan con consentimiento.

## Archivos modificados

- `index.html`
- `styles.css`
- `docs/cookies.html`

## Nota técnica

La app sigue siendo una web estática y sencilla de desplegar en GitHub Pages. Los cambios están pensados para mejorar robustez y cumplimiento básico sin introducir build tools ni dependencias nuevas.

## Segunda pasada: diseño responsive y copy

- Se mejora la cabecera con una propuesta de valor más clara.
- El botón principal pasa de `Play` a `Empezar`.
- La pantalla inicial explica mejor qué hace la app y qué esperar de cada partida.
- La pantalla de temas incluye una introducción más útil.
- La pantalla de resultados añade mensaje de desempeño, tarjetas de métricas y acción directa para repetir el mismo cuestionario.
- Se refina el estilo visual con contenedores tipo panel, mejor espaciado, jerarquía tipográfica y una adaptación móvil más cuidada.
