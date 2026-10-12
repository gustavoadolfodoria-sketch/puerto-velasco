# Puerto Velasco · Barbería

Sitio estático de una sola página en HTML5 y CSS3. Sin JavaScript, dependencias ni compilación.

## Archivos

- `index.html`: contenido, enlaces y metadatos.
- `styles.css`: estilos adaptables y variables de color.
- `assets/`: tres fotografías propias optimizadas a JPEG y un favicon tipográfico SVG (no es un logo oficial).

Abre `index.html` en un navegador para ver la web. Mantén los archivos y la carpeta assets en la misma ubicación.

## Decisiones y datos pendientes

Se usa **Puerto Velasco**, tal como aparece en la fachada. El texto del encargo dice «PUERO VELAZCO»: confirmar la escritura definitiva antes de publicar.

El horario lunes a domingo, 9 a. m. a 7 p. m., y «Est. 2022» se transcribieron del letrero de la fotografía. Confirmar que siguen vigentes.

No se proporcionaron servicios, precios, fotos de cortes ni testimonios verificables. Se incluye una sección de consulta de servicios y las fotos del espacio; no se publica un catálogo ficticio ni puntuaciones o reseñas inventadas. Para completar el catálogo, entregar nombre, descripción, precio (opcional) y fotografía de cada servicio. La foto del mostrador es de ambiente, no evidencia de un corte.

El botón de reseñas abre el enlace de Google suministrado. No se obtuvo un enlace directo para escribir una reseña ni se verificó la ficha de destino. Confirmar manualmente que el enlace corresponde al negocio y permite acceder a sus reseñas. Si se obtiene un enlace directo de reseñas, sustituir el destino del primer botón. Confirmar ubicación exacta y URL final de publicación.

## Personalización

1. Edita los textos y enlaces en `index.html`.
2. Cambia los colores en las variables de `:root` en `styles.css`.
3. Reemplaza las imágenes conservando los nombres o actualiza sus rutas, dimensiones y textos alternativos.
4. Para añadir servicios reales, crea bloques dentro de `#servicios` con su fotografía, nombre, descripción y enlace WhatsApp específico. No añadir datos de ejemplo a la web publicada.
5. WhatsApp usa `https://wa.me/573133165733` (sin `+`, espacios ni signos). Los mensajes se encuentran en el parámetro `text`, codificados para URL.
6. Una vez tengas la URL real, añade en `<head>`:

```html
<meta property="og:url" content="URL_ABSOLUTA_REAL_DEL_SITIO">
<meta property="og:image" content="URL_ABSOLUTA_REAL_DEL_SITIO/assets/fachada.jpg">
<link rel="canonical" href="URL_ABSOLUTA_REAL_DEL_SITIO">
```

Sustituye los valores antes de añadirlos. Los marcadores anteriores son instrucciones y no están incluidos en el sitio. No hay URL ficticia en el HTML.

## Subir a GitHub

1. En GitHub, pulsa **New repository**, elige un nombre como `puerto-velasco` y crea el repositorio.
2. Elige **Add file → Upload files**.
3. Sube el contenido de esta carpeta: `index.html`, `styles.css`, `README.md` y `assets/`. `index.html` debe estar en la raíz del repositorio.
4. Confirma la subida con **Commit changes**. No subas solo el ZIP: extrae su contenido primero.

## Desplegar en Vercel

1. En Vercel, elige **Add New → Project** y conecta tu cuenta de GitHub.
2. Importa el repositorio.
3. Selecciona **Other** como Framework Preset y la raíz del repositorio como Root Directory.
4. Deja Build Command sin comando (si aparece uno, activa su opción de modificación y déjalo vacío). No se necesitan Install Command ni dependencias.
5. Usa la raíz como Output Directory (`.` si el panel solicita un valor).
6. Pulsa **Deploy**. Abre el dominio obtenido y completa los metadatos de publicación con esa URL.

No se incluye `vercel.json`: un sitio con `index.html` en la raíz no necesita rutas especiales ni configuración adicional. Las nuevas confirmaciones en GitHub pueden desplegarse automáticamente mediante la integración.

## Verificación

Realizado: comprobación local de rutas HTML/CSS/imágenes, destinos no vacíos, número y mensajes de WhatsApp, enlaces internos y `rel="noopener noreferrer"` en enlaces externos. La entrega no contiene JavaScript ni formularios simulados. Fotografías reducidas a un máximo de 1400 px y comprimidas; imágenes secundarias con carga diferida. CSS con Grid, media queries, foco visible y reducción de movimiento.

Pendiente: revisión visual en navegador a 320, 375, 768 y 1440 px (incluyendo desbordamiento horizontal y legibilidad); comprobar que los destinos externos corresponden al negocio, la ficha y reseñas de Google; confirmar datos comerciales; probar despliegue en una cuenta real de Vercel y vista previa de Open Graph tras completar URLs. La revisión de código no sustituye estas comprobaciones.
