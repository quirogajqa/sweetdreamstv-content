# Sweet Dreams TV — Catálogo de ambientes

Esta carpeta está preparada para ser un repositorio público independiente. Contiene únicamente `catalog.json` y las imágenes WebP de reproducción. No incluye código de la app, credenciales, APKs ni PNG originales.

## Publicación

Publicar el contenido de esta carpeta en la raíz de un repositorio público. Usar la URL HTTPS del archivo RAW `catalog.json` como propiedad Gradle:

`-PsweetDreamsCatalogUrl=https://raw.githubusercontent.com/quirogajqa/sweetdreamstv-content/main/catalog.json`

También se puede agregar `sweetDreamsCatalogUrl=...` a `gradle.properties`. Para migrar de alojamiento basta cambiar esta URL y mantener las rutas relativas del catálogo.

## Formato v1

El catálogo incluye versión de esquema, versión de catálogo, ID/nombre/descripción del ambiente, acceso Premium, versión del pack, ID de portada y lista de imágenes con URL relativa, tamaño y SHA-256.

Incrementar la versión del pack cuando cambien sus imágenes. Publicar primero los archivos, y después el catálogo actualizado. Mantener archivos de versiones anteriores para dispositivos que aún los usan.

Las imágenes de Luna y estrellas fueron generadas mediante ImageGen para Sweet Dreams TV. Resolución de reproducción: 1600 × 900, WebP.
