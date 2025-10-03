# Docentes Brown — Sitio estático

Este repo contiene la landing con:
- Carrusel de **Noticias** arriba (3 principales con auto‑deslizamiento cada 5s y loop).
- Sección **Herramientas** (Tienda, Concursos, Calculadora, Particulares).
- Sección **Podcast** con **Spotify embed** y animación decorativa de ecualizador.
- Sección **Noticias** con paginación y **RSS**.
- Zócalo **Sumate** clickeable (lleva al formulario).
- Botones flotantes de **WhatsApp** y **Cafecito**.
- **Modo oscuro** con toggle.

## Estructura de archivos
```
index.html
news.json          # (opcional) noticias, si no existe se usa fallback
podcasts.json      # (opcional) episodios, si no existe se usa fallback
/podcasts/         # (opcional) si en algún momento querés audios locales
```

## Publicación en GitHub Pages
1. Crear repo público en GitHub.
2. Subir `index.html`, `news.json`, `podcasts.json` (opcional).
3. En **Settings → Pages**: Source `Deploy from a branch`, branch `main`.
4. Abrir la URL `https://USUARIO.github.io/NOMBRE-REPO/`.

## Cargar Noticias
Editar `news.json` (array). Campos:
- `titulo` (string), `fecha` (YYYY-MM-DD), `link` (URL), `resumen` (string), `img` (URL opcional).
Las 3 más recientes (por `fecha`) van al carrusel superior; el resto aparece abajo con paginación.

## Cargar Podcast
Editar `podcasts.json` (array). Campos:
- `titulo`, `fecha`, `spotify` (URL a show/episode), `descripcion`.
El sitio transforma `spotify` a `embed` automáticamente.

## Personalización rápida
- Colores: variables CSS en `:root` (`--azul`, `--violeta`, etc.).
- Intervalo del carrusel: modificar `setInterval(carouselNext, 5000)` en `index.html`.
- Tienda / links: editar tarjetas en la sección **Herramientas**.
