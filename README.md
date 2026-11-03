# Órbita Escolar

Plataforma de juegos educativos para primaria. Cada juego es una aplicación web instalable (PWA) que funciona sin conexión.

## Juegos

| Juego | Carpeta | Materia |
| --- | --- | --- |
| Patrulla Numérica | `juegos/patrulla-numerica/` | Matemáticas, 1.º a 6.º de primaria |
| Palabra Secreta | `juegos/palabra-secreta/` | Lengua, 2.º de primaria |

La portada (`index.html`) es provisional: enlaza a los juegos mientras se diseña la plataforma común.

## Publicar en GitHub Pages

1. *Settings → Pages → Source: Deploy from a branch*, rama `main`, carpeta `/ (root)`.
2. La plataforma queda en `https://jvlsile.github.io/orbita-escolar/` y cada juego en su carpeta.

## Actualizar un juego

Cambia sus archivos y sube el número `VERSION` de su `sw.js`, para que los dispositivos que ya lo tienen instalado descarguen la versión nueva.

## Origen

- Patrulla Numérica: copia de `jvlsile/invasoresnumericos`, actualizada a la versión v20 (flotación de las naves, explosiones nuevas, repaso de fallos y jefes sin escolta).
- Palabra Secreta: copia de `jvlsile/palabra-secreta`, sin cambios.

Los repositorios originales no se han modificado.
