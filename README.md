# La Bianca — Landing Page

Sitio estático (HTML/CSS/JS vanilla, sin build ni dependencias). Listo para abrir en Cursor o cualquier editor.

## Estructura
```
index.html       → toda la página (estructura, estilos y JS inline)
favicon.svg       → favicon del sitio, ya enlazado en el <head>
images/           → todas las fotos y no debe separarse de index.html
```

## Cómo verlo local
Simplemente abrí `index.html` en el navegador (doble click), o con Live Server
si usás la extensión de VSCode/Cursor.

## Cómo deployar
- **Netlify Drop**: arrastrá esta carpeta completa (con `images/` y `favicon.svg`
  incluidos) a https://app.netlify.com/drop
- **Vercel**: subí este mismo contenido a un repo de GitHub y hacé "Import Project"
  en vercel.com. Al ser HTML estático no requiere configuración de build.

⚠️ Importante: `images/` y `favicon.svg` siempre deben viajar junto a `index.html`.
Las rutas del código son relativas (`images/nombre.jpg`), así que si se sube solo
el HTML sin la carpeta, las fotos no van a cargar.

## Pendientes / notas
- El mapa de Google Maps usa el método gratuito `output=embed` (sin API key). Si en algún
  momento deja de renderizar, la alternativa 100% garantizada es reemplazar el `src`
  del `<iframe id="mapFrame">` por el que te da Google en Maps → Compartir →
  "Insertar un mapa" → Copiar HTML (también gratis, sin key).
- El dominio real todavía no está seteado: buscar `lacaslabianca.com.ar` en el
  `<head>` (canonical, Open Graph, JSON-LD) y reemplazar por el dominio definitivo
  una vez que lo tengan.
- El número de WhatsApp usado es `5491127893750` — confirmar que sea el correcto
  antes de producción (aparece en el botón flotante).
