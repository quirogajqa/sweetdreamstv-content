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

## Ambientes disponibles

- Luna y estrellas: 12 imágenes, pack 2.
- Bosque nocturno: 6 imágenes, pack 1.
- Océano nocturno: 6 imágenes, pack 1.
- Auroras boreales: 6 imágenes, pack 1, Premium (`sweet_dreams_auroras`).
- Bosque encantado: 6 imágenes, pack 1, Premium (`sweet_dreams_bosque_encantado`), requiere app 1.2.0 o posterior.

Los cinco packs fueron generados con ImageGen para Sweet Dreams TV y se distribuyen en WebP de 1600 × 900.


Los packs Premium incluyen `premium: true` y `productId` de Google Play. La app verifica la compra para permitir descarga y reproducción. Este repositorio es público: las URL de las imágenes no son privadas. Se necesita Sweet Dreams TV 1.1.0 o posterior para comprar Auroras boreales.

Desde Sweet Dreams TV 1.2.0, los productos Premium se descubren directamente de `productId` en el catálogo. Consulta [cómo agregar un pack sin actualizar la app](NUEVOS_PACKS.md).
