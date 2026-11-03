# Sonido opcional por ambiente

Solo los ambientes con `sound: true` reproducen audio. Omitir el campo o usar `sound: false` mantiene el pack sin sonido. No es necesario agregar audio a todos los ambientes.

Con `sound: true`, `pack.audio` debe indicar `url` (HTTPS de un Ogg Vorbis en bucle), `bytes`, `sha256`, `title`, `author`, `source`, `license`, `licenseUrl` y `changes`. El archivo puede pesar hasta 32 MiB; el pack completo hasta 128 MiB. Aumentar `pack.version` cuando cambien imágenes o audio, conservando las rutas publicadas anteriores.

Las imágenes y el audio se descargan y verifican antes de activar la nueva revisión. Una revisión anterior sigue funcionando mientras se descarga la actualización. La app conserva el control de sonido por ambiente, reproduce localmente en bucle, reduce el volumen durante el oscurecimiento final y libera el reproductor al salir o pasar a segundo plano.

En el detalle de un ambiente con audio descargado, abrir «Sonido ambiental» para activarlo/desactivarlo y consultar la atribución. El volumen se controla con el mando del televisor.

La reproducción requiere Sweet Dreams TV 1.3.0 o posterior. Las versiones anteriores ignoran el audio. Bosque encantado v2 incorpora la grabación de aldeainvisible (CC BY 4.0), con atribución en `packs/enchanted/2/CREDITOS.txt` y dentro de la app. La licencia del audio original sigue vigente; no se reclama exclusividad sobre él.
