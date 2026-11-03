# Agregar un ambiente sin actualizar la app

Requiere Sweet Dreams TV 1.2.0 o posterior. Los dispositivos con versiones anteriores deben actualizar una vez.

1. Para un ambiente Premium, crear en Google Play Console un producto único, opción Comprar (no alquiler), una sola unidad, y activar sus precios y países. Cada pack debe tener su propio ID de producto. Los packs gratuitos omiten este paso.
2. Preparar las imágenes WebP (recomendado 1600 × 900). Publicarlas primero en `packs/ID_DEL_PACK/VERSION/`.
3. Calcular el tamaño exacto en bytes y SHA-256 de cada archivo.
4. Agregar el ambiente a `collections` en `catalog.json`: `id`, `name`, `description`, `detailedDescription`, `premium` y, si es Premium, `productId` exactamente como aparece en Play Console. En `pack` indicar `version`, `coverId` y `images` con `id`, `url` relativa, `bytes` y `sha256`.
5. Aumentar `catalogVersion` y publicar el JSON cuando todos los archivos estén accesibles.
6. En la TV, actualizar ambientes (o volver a abrir la app). La app descubrirá los productos del catálogo y consultará sus precios a Google Play; la compra se verificará antes de permitir descargar y reproducir.

No se necesita cambiar código, recompilar ni publicar otro AAB para agregar nuevos packs. La compra no se concede por aparecer en el JSON: exige un comprobante firmado por Google Play para el mismo paquete y producto.

## Reglas de mantenimiento

- Mantener estables el ID del ambiente y su productId después de venderlo. Un producto no puede asignarse a dos ambientes del catálogo.
- Para agregar o reemplazar imágenes de un pack existente, aumentar `pack.version`, publicar una carpeta de versión nueva y conservar los archivos anteriores.
- Nunca convertir los tres ambientes gratuitos originales en productos pagos.
- Un producto inexistente o todavía no disponible en Google Play no tendrá botón de compra habilitado, sin bloquear los demás packs.
- Las compras restauradas se conservan aunque el catálogo no esté disponible; el uso offline requiere haber descargado las imágenes.
- Este repositorio es público. La app controla el desbloqueo; las URL no son un sistema privado de entrega de contenido.
