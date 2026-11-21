# Suite Soho – sitio web

Sitio de una sola página de **Suite Soho**, departamento de alquiler temporario en Honduras 4154, Palermo, Buenos Aires.

Es HTML estático: no tiene frameworks ni paso de compilación. Lo que está en la rama `main` es lo que se publica.

## Estructura

```
index.html          Página completa (estilos dentro del mismo archivo)
img/                Fotos, logo, íconos e imagen para compartir
robots.txt
```

## Publicación automática

El repositorio está pensado para conectarse a **Cloudflare Pages** (sirve igual Netlify):

- Framework preset: **None**
- Build command: *(vacío)*
- Build output directory: `/`

Con eso, cada cambio que se sube a `main` se publica solo en uno o dos minutos. Cada rama distinta de `main` genera una vista previa con su propia URL.

## Cómo hacer cambios

- **Textos:** editar `index.html`. Cada sección tiene su `id`: `inicio`, `depto`, `edificio`, `ubicacion`, `resenas`, `reservar`.
- **Fotos:** reemplazar el archivo en `img/` manteniendo el nombre, o agregar uno nuevo y cambiar el `src` en `index.html`.
- **Colores de marca:** dorado `#CDA047` (botones), dorado claro `#DFB051` (texto sobre fondo oscuro), bronce `#7A5A14` (enlaces sobre fondo claro), gris `#3A3F3D` (fondos oscuros).
- **Tipografías:** Cinzel para títulos y Sofia Sans para el texto, desde Google Fonts.

## Pendientes

- La web está publicada en https://suite-soho-web.mandrioli.workers.dev. Cuando haya dominio propio, reemplazar esa dirección en `og:url`, `og:image`, `canonical` y en `image` y `url` del bloque `application/ld+json`.
- Reemplazar las fotos por los originales en alta resolución (las actuales salen de las publicaciones, de unos 1150 px).
- Reemplazar el logo por el archivo original (SVG o PNG sin fondo).
- Las cifras de reseñas (9,9 con 101 comentarios en Booking, 5,0 con 16 reseñas en Airbnb, 117 estadías con reseña, 13 países) son del 20/11/2026 y conviene actualizarlas cada tanto.
- El mapa usa el formato de inserción de Google Maps que no necesita clave. Si algún día deja de mostrarse, se puede reemplazar por el iframe que da Google Maps en **Compartir → Insertar un mapa**.
