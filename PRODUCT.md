# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

delegated: HTML, CSS y JavaScript estáticos, sin herramientas de compilación. Cada archivo se sube tal cual a GitHub Pages (`jvlsile.github.io/orbita-escolar/`), igual que los juegos, y funciona sin conexión cuando se instala como app. Elegido porque los juegos ya siguen este formato y el autor los mantiene editando y subiendo archivos.

## Users

Alumnos de primaria (6-12 años), en español de España. Dos situaciones principales:

- **Pizarra digital en clase:** el docente proyecta la portada y el grupo elige juego. Se ve desde lejos y se toca con el dedo o el lápiz de la pizarra.
- **En casa:** el alumno entra solo desde un móvil, una tableta o el ordenador familiar.

El docente y la familia son usuarios secundarios: abren la portada para elegir o recomendar un juego.

## Product Purpose

Órbita Escolar reúne en un solo sitio los juegos educativos del autor. La portada lleva a cada juego y debe dejar claro que la colección crecerá: hoy hay dos juegos y vendrán más.

## Positioning

Colección propia de juegos para primaria creada por un docente para usarla en su aula: gratis, sin cuentas, sin anuncios y sin enviar datos. Cada juego funciona sin conexión.

## Operating Context

- Juegos actuales: **Patrulla Numérica** (matemáticas, 1.º a 6.º; naves espaciales con operaciones) y **Palabra Secreta** (lengua, 2.º; el búho detective Lupi da pistas para descubrir una palabra).
- Cada juego vive en `juegos/<nombre>/` como app instalable independiente, con su propia identidad visual, fuentes e iconos.
- El progreso de cada juego se guarda en el propio dispositivo (localStorage). No hay servidor.

## Capabilities and Constraints

- Sitio estático en GitHub Pages; nada de servicios externos ni fuentes cargadas de Google (los juegos ya incluyen sus fuentes).
- Debe funcionar en pizarras digitales y tabletas escolares antiguas.
- Sin datos personales.
- Pendiente de decidir: perfiles comunes, estrellas compartidas entre juegos y modo docente.

## Brand Commitments

- Nombre: **Órbita Escolar**.
- Los juegos conservan sus nombres e identidades (Patrulla Numérica, Palabra Secreta, Lupi).

## Evidence on Hand

- Iconos de los juegos: `juegos/patrulla-numerica/icons/`, `juegos/palabra-secreta/icons/`.
- No hay testimonios, cifras de uso ni opiniones de colegios: no inventarlos.

## Product Principles

1. Elegir juego en un toque, también desde el fondo del aula.
2. Que la colección se sienta viva y con sitio para más juegos.
3. Cero fricción: sin registro, sin anuncios, sin conexión obligatoria.
4. Cada juego conserva su personalidad; la plataforma los acoge sin uniformarlos.

## Accessibility & Inclusion

Lectores que empiezan (6-7 años): textos cortos y claros. Objetivos táctiles grandes. Respetar «reducir movimiento». Buen contraste en proyectores con poca luz.
