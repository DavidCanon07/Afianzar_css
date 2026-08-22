# Repaso CSS — Flexbox, Box Model y Responsive Design

Ejercicio práctico de repaso desarrollado para el curso **Tecnología en Desarrollo de Software
(IV Semestre)**, enfocado en afianzar Flexbox, Media Queries y el Box Model de CSS3.

Página de una sola vista con 3 tarjetas en fila, cada una mostrando un proyecto real del autor,
con un tratamiento visual tipo "ventana de terminal" (coherente con que los 3 proyectos son
herramientas de automatización/línea de comandos).

## Ejercicios cubiertos

1. **Flexbox**: 3 tarjetas en fila (`display: flex`), cada una con título, descripción y un color
   de fondo distinto.
2. **Media Query**: por debajo de 768px las tarjetas se apilan verticalmente al 100% del ancho.
3. **Box Model + sombra**: padding, margin, border y `box-shadow` para dar profundidad a las
   tarjetas.

## Tecnologías

- HTML5 semántico (`header`, `main`, `article`, `footer`).
- CSS3: Box Model, variables CSS (`:root`), Flexbox, Media Queries, `@keyframes` (cursor
  parpadeante, respeta `prefers-reduced-motion`).
- Sin frameworks, sin librerías externas ni CDNs. Sin JavaScript.

## Estructura del proyecto

```
├── index.html          # Estructura de la página y contenido de las tarjetas
├── CSS/
│   └── Style.css         # Estilos, paleta de color y responsive
├── README.md
└── PROMPT.md              # Prompt de apoyo usado con IA (evidencia del proceso)
```

## Diseño responsive

| Dispositivo        | Ancho    | Comportamiento                  |
|---------------------|----------|----------------------------------|
| Escritorio / Tablet | ≥ 768px  | 3 tarjetas en fila (Flexbox)     |
| Móvil                | < 768px  | Tarjetas apiladas, 100% de ancho |

## Cómo verlo

No requiere instalación ni servidor: basta con abrir `index.html` en cualquier navegador. Para
probar el breakpoint, usar el modo responsive de las DevTools (`F12` → `Ctrl+Shift+M`).

## Proceso de creación

Ejercicio desarrollado con apoyo de un asistente de IA (Claude Code), tomando como referencia de
estructura y documentación el proyecto de portafolio ["Maquetado"](https://github.com/DavidCanon07/ejercicios-maquetado).
El prompt utilizado, junto con las decisiones de contenido y diseño, está documentado en
[PROMPT.md](PROMPT.md).

## Autor

**David Cañón**
