# Prompt de apoyo utilizado (IA generativa)

Este archivo documenta el prompt utilizado como apoyo de un asistente de IA (Claude Code) para
la creación de este ejercicio de repaso, como evidencia del proceso para el docente del curso.

## Prompt utilizado

```
Contexto: Proyecto académico de maquetación web desarrollado en IV semestre de Tecnología en Desarrollo de Software. Consiste en la creación de un portafolio personal utilizando HTML5 semántico y CSS3 puro, aplicando conceptos de Box Model, Flexbox, CSS Grid, variables CSS y diseño responsive mediante Media Queries. El proyecto no utiliza frameworks ni librerías externas y está estructurado para adaptarse a dispositivos móviles, tabletas y computadores. El desarrollo contó con apoyo de IA mediante Claude Code, dejando documentado el prompt utilizado como parte de la evidencia del proceso.

Rol: Actúa como Wed designer & software engineer.

Objetivo: Afianzar los conceptos de CSS y responsive design mediante ejercicios prácticos.

Acción:

Realiza los siguientes ejercicios prácticos en un mismo archivo HTML (puedes incluir el CSS en el `<head>` o en un archivo externo):

1. **Ejercicio 1:** Crea una página con 3 tarjetas en fila usando **Flexbox**. Cada tarjeta debe tener un título, una descripción breve y un color de fondo diferente.
2. **Ejercicio 2:** Agrega una **media query** para que en móvil (pantallas menores a 768px) las tarjetas se apilen verticalmente y ocupen el 100% del ancho.
3. **Ejercicio 3:** Aplica **box model** a las tarjetas (padding, margin, border) y agrega sombras (`box-shadow`) para darles profundidad.

Criterios:

- legible y muy clara
- sencilla aplicando el método KISS

Restricciones:

- Utiliza: HTML5 y CSS3.
- No utilices: algún framework o concepto fuera del alcance planteado, tampoco emojis cambialos por simbolos.
- No asumas: que es un programa elaborado.

Salida:

- el archivo `index.html` y Style.css en la carpeta "Ejercicio_repaso_CSS"
- al repo https://github.com/DavidCanon07/Afianzar_css se debe subir el proyecto
```

## Insumo adicional aportado en la conversación

- Se pidió tomar el proyecto de portafolio ["Maquetado"](https://github.com/DavidCanon07/ejercicios-maquetado)
  como referencia de estructura, contenido y documentación (carpeta `CSS/`, `README.md`,
  `PROMPT.md`).
- Se pidió usar proyectos reales del GitHub del autor como contenido de las 3 tarjetas, en vez de
  contenido genérico: `conexion_directa`, `automatizacion-ops` y `conexion_directa_conciso`
  (este último repo privado; su descripción funcional fue aportada directamente por el autor).
- Se invocó el skill `frontend-design` y se aprobó explícitamente una dirección visual distintiva
  (tarjetas estilo "ventana de terminal") en lugar de reutilizar la paleta plana de Maquetado.

## Decisiones tomadas por la IA (resumen)

- **Flexbox** para la fila de 3 tarjetas (`display: flex`, `flex: 1` en cada tarjeta), tal como
  pide el Ejercicio 1.
- **Media Query única** en `max-width: 767px` (Ejercicio 2): cambia `flex-direction` a `column` y
  cada tarjeta pasa a `width: 100%`.
- **Box Model + `box-shadow`** en cada tarjeta (Ejercicio 3): `padding`, `border` y una sombra
  tipo "ventana flotante" para dar profundidad.
- **Dirección visual "terminal/ventana"**: cada tarjeta simula una ventana de terminal (barra de
  puntos, línea de comando como título en fuente monoespaciada del sistema), coherente con que
  los 3 proyectos reales son herramientas CLI de automatización. Un cursor parpadeante (`▍`) en
  el encabezado funciona como elemento de firma visual, implementado en CSS puro
  (`@keyframes`) y desactivado con `prefers-reduced-motion: reduce`.
- **Paleta**: 3 fondos de tarjeta en tonos pastel derivados de una paleta fría (teal, ámbar,
  índigo) en vez de colores planos saturados, para cumplir "color de fondo diferente por
  tarjeta" sin perder legibilidad ni cohesión visual.
- Sin frameworks, sin CDNs, sin JavaScript. Sin emojis: los símbolos usados (`▍`, `●`, `→`) son
  caracteres Unicode, no emoji.
