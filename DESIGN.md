---
name: Órbita Escolar
description: Base de lanzamiento al anochecer donde cada juego es un cohete en su rampa.
colors:
  night: "#121844"
  dusk: "#2B2569"
  plum: "#5E3878"
  ember: "#D9694A"
  glow: "#F7A55A"
  ink: "#1E2033"
  ink-2: "#4A4C66"
  paper: "#FFFDF7"
  concrete: "#ECE5D6"
  concrete-2: "#DDD3BF"
  lemon: "#FFD23F"
  star: "#F6F1FF"
  star-2: "#C9C3F2"
  go: "#2FBF71"
  slot-ink: "#6B6250"
typography:
  display:
    fontFamily: "Fredoka, Andika, ui-rounded, system-ui, sans-serif"
    fontSize: "clamp(2.3rem, 5.6vw, 4.6rem)"
    fontWeight: 700
    lineHeight: 1.02
    letterSpacing: "-0.025em"
  title:
    fontFamily: "Fredoka, Andika, ui-rounded, system-ui, sans-serif"
    fontSize: "clamp(1.45rem, 2vw, 1.8rem)"
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: "-0.01em"
  label:
    fontFamily: "Fredoka, Andika, ui-rounded, system-ui, sans-serif"
    fontSize: "0.95rem"
    fontWeight: 600
    lineHeight: 1.3
  body:
    fontFamily: "Andika, system-ui, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 400
    lineHeight: 1.5
rounded:
  pill: "999px"
  plate: "20px"
  panel: "24px"
  deck: "6px"
spacing:
  gutter: "clamp(16px, 4vw, 48px)"
  pad-gap: "clamp(14px, 2vw, 28px)"
  plate: "18px"
  stage: "clamp(230px, 34vh, 330px)"
components:
  button-launch:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.lemon}"
    typography: "{typography.title}"
    rounded: "{rounded.pill}"
    height: "56px"
  plate-game:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.plate}"
    padding: "18px"
  plate-slot:
    backgroundColor: "transparent"
    textColor: "{colors.ink-2}"
    rounded: "{rounded.plate}"
    padding: "18px"
  chip-subject:
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "3px 12px"
  console:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.star}"
    rounded: "{rounded.panel}"
---

# Design System: Órbita Escolar

## Overview

La portada es una base de lanzamiento vista de perfil al anochecer. Arriba, el cielo (añil con estrellas y un planeta con su órbita); en el horizonte, una franja de seguridad amarilla y negra; abajo, el hormigón de la base. Cada juego es un cohete en su rampa, pintado con los colores de su propio juego, con su icono en el ojo de buey. Elegir juego es despegar: al tocar una rampa el cohete sale disparado y se abre el juego. Las rampas vacías, con el cohete dibujado a trazos, dicen que vendrán más juegos.

Público: alumnos de 6 a 12 años en la pizarra digital y en casa. Textos cortos, objetivos táctiles grandes, contraste alto.

## Colors

### Primary
- **Ink `#1E2033`**: texto, contornos de cohetes y placas, torres, panel de consola.
- **Lemon `#FFD23F`**: franja de seguridad, anillo del foco, «Escolar» en el rótulo.

### Neutral
- **Concrete `#ECE5D6`**: suelo de la base, fondo de todo lo que queda bajo el horizonte. Es material del mundo, no un crema de plantilla.
- **Paper `#FFFDF7`**: placas de rampa activas.
- **Ink-2 `#4A4C66`**: texto secundario sobre hormigón y papel.

### Sky ramp
`night #121844 → dusk #2B2569 → plum #5E3878 → ember #D9694A → glow #F7A55A`. Solo para el cielo; ningún texto se apoya en el tramo plum–glow.

### Named Rules
- **Cada juego trae su pintura.** Los colores de un cohete (`--hull`, `--nose`, `--fin`, `--trim`) y de su botón (`--go-bg`, `--go-ink`) vienen de la identidad del juego (Patrulla: añil y limón; Palabra Secreta: azul #2440C8 y ámbar). La plataforma solo pone el hormigón, el cielo y la tinta.
- **Verde solo en luces.** `go #2FBF71` aparece únicamente en los pilotos del panel.

## Typography

- **Fredoka 600/700** para rótulos, títulos de rampa, botones y etiquetas.
- **Andika 400/700** (tipografía pensada para lectores que empiezan) para todo el texto de lectura.
- Ambas autoalojadas en `fonts/`; nada de Google Fonts.

### Hierarchy
Display (pregunta principal) → title (nombre del juego, 1,45–1,8 rem) → label (asignatura y curso) → body 1,125 rem. Medida máxima del cuerpo: 68ch.

## Layout

- Cielo a ancho completo; contenido centrado a 1240 px con margen `gutter`.
- Plataforma: rejilla de 4 rampas en escritorio. Por debajo de 1020 px, la fila se desliza en horizontal con imán (scroll-snap) y la siguiente rampa asoma; en móvil cada rampa ocupa el 74 % del ancho.
- La altura del escenario (`stage`) gobierna cohete (40 % de ancho), torre (80 % de alto) y la línea del horizonte.

## Elevation & Depth

- Placas: `0 14px 28px -12px rgba(30,32,51,.45)` (sombra suave desplazada hacia abajo).
- Panel de consola: `0 18px 36px -18px rgba(30,32,51,.6)`.
- Botón de despegue: bisel interior inferior `inset 0 -5px 0 rgba(0,0,0,.22)` que se reduce al pulsar.
- Pilotos: halo verde; es una luz encendida, el único brillo permitido.

## Shapes

Formas redondeadas y gruesas: contornos de 3–3,5 px en tinta, placas de 20 px de radio, botones en píldora. Las rampas futuras usan contorno discontinuo.

## Components

### Rampa de juego (signature)
`li.pad.g-<juego> > a` envuelve el escenario (torre, plataforma, humo, cohete con ojo de buey) y la placa (título, chip de asignatura y curso, frase, botón «Despegar»). Toda la rampa es un único enlace. Al pulsar: temblor de 0,28 s, llama, humo y despegue `cubic-bezier(.55,0,.85,.35)` 1,15 s; se navega a los 1,05 s. Con «reducir movimiento» se navega al instante. Ctrl/Cmd-clic abre en pestaña nueva sin animación.

Para añadir un juego: duplicar un `li.pad`, cambiar `href`, icono, textos y definir su clase `.g-<juego>` con sus colores; sustituir una rampa vacía.

### Rampa vacía
`li.pad > .slot`: torre atenuada, cohete fantasma discontinuo, placa transparente con borde discontinuo, «Rampa N · Próximo lanzamiento».

### Botón de despegue
Píldora de 56 px de alto, Fredoka 700 1,3 rem, flecha hacia arriba en SVG. Colores del juego.

### Panel «Informe de la base»
Consola en tinta con pilotos verdes; cada línea: título corto en Fredoka y explicación en Andika.

### Navigation
Rótulo con planeta anillado a la izquierda; enlace «Docentes y familias» subrayado a la derecha, que baja al informe.

## Do's and Don'ts

### Do:
- Mantener una sola animación protagonista: el despegue. El satélite gira despacio y se detiene con «reducir movimiento».
- Usar textos de una línea para los alumnos («Toca un cohete para empezar a jugar»).
- Dejar al menos una rampa vacía visible para que la colección parezca abierta.

### Don't:
- No poner texto sobre el degradado del horizonte.
- No convertir las rampas en tarjetas genéricas con icono, título y texto.
- No uniformar los cohetes: cada juego conserva su color.
- No añadir etiquetas encima de los títulos ni iconos hechos con emojis.
