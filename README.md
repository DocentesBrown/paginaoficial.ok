# Docentes Brown — Sitio estático (instrucciones rápidas)

Incluye:
- **Carrusel de Noticias** arriba (3 principales, auto cada 5s, vuelve a la primera).
- **Podcast con Spotify embebido** (usa URL de episode/show y lo convierte a /embed/).
- **Herramientas** (Tienda, Concursos, Calculadora, Particulares).
- **Noticias** con paginación + **RSS**.
- **Zócalo Sumate** clickeable (formulario).
- **WhatsApp** y **Cafecito** actualizados.
- **Modo oscuro** con toggle (persistencia en localStorage).

## Archivos
```
index.html
news.json          # noticias (si no está, usa fallback)
podcasts.json      # episodios (si no está, usa fallback)
```

## Cómo cargar noticias
Editar `news.json` con objetos:
```json
{ "titulo":"...", "fecha":"2025-10-03", "link":"https://...", "resumen":"...", "img":"" }
```
Las 3 más recientes van al carrusel superior; el resto aparece abajo con paginación.

## Cómo cargar podcast
Editar `podcasts.json` con objetos:
```json
{ "titulo":"...", "fecha":"2025-10-01", "spotify":"https://open.spotify.com/episode/XXXXXXXX", "descripcion":"..." }
```
El sitio embebe automáticamente usando `/embed/` para escuchar en la página.

## Publicar en GitHub Pages
1) Repo público → subir `index.html`, `news.json`, `podcasts.json` (opcional).  
2) **Settings → Pages** → Deploy from a branch → branch `main`.  
3) Visitar `https://TU-USUARIO.github.io/NOMBRE-REPO/`.
