# Under the Plate — sitio publicable

Contenido listo para GitHub Pages con dominio propio (undertheplate.xyz).

## Publicar (una vez)
1. Crea un repositorio en GitHub (p. ej. `under-the-plate`).
2. Sube TODO el contenido de esta carpeta a la raiz del repo
   (incluye `.nojekyll`, `CNAME`, `assets/`, `img/`).
3. Settings -> Pages -> Source: Deploy from a branch -> `main` / `(root)`.
4. Settings -> Pages -> Custom domain: `undertheplate.xyz` -> Enforce HTTPS.

## DNS (en tu proveedor del dominio)
- `@` (raiz): 4 registros **A** ->
  `185.199.108.153` · `185.199.109.153` · `185.199.110.153` · `185.199.111.153`
- `www`: registro **CNAME** -> `TU-USUARIO.github.io`

## Despues de publicar
- Registra el dominio en Google Search Console y envia `sitemap.xml`.

## Actualizar el sitio
```
python3 tools/make_responsive.py && python3 tools/make_recipe.py && python3 tools/make_web.py
```
(desde la carpeta del proyecto; vuelve a subir el contenido de `web/`)
