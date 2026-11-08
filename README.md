# ZoneMap

A client minimap and world map with terrain layers, markers, radar and optional server integrations. Beta38 improves the reconstructed tilted terrain while retaining the top-down view.

Minimapa y mapa grande con capas, marcadores, radar e integraciones opcionales. Beta38 mejora el terreno inclinado reconstruido y conserva la vista cenital.

## Current release / Entrega actual — 2026-11-08

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 1.0.0-beta38 |
| Client / Cliente | 1.0.0-beta38 |

**Protocol / Protocolo:** zonemap-3.

[Downloads / Descargas](https://www.curseforge.com/projects/1738053/files) · [Release / Novedades](RELEASE-2026-11-08.md) · [Configuration / Configuración](CONFIGURATION.md)

## English

Minecraft 1.20.1, Forge 47.4.x, Java 17. ZoneCore 2.1.2–2.x is required only for ZoneMap Server. Install one side JAR per instance; beta38 keeps protocol zonemap-3.

Beta38 includes textured side faces and verified lower exterior surfaces beneath floating objects. It repairs missing walls beneath partial roofs such as slabs/stairs, preserves real transparency, excludes invisible terrain blocks and keeps visible facades behind nearby floating roofs. Style changes refresh received tiles; ZMT25 migrates readable older cache data without deleting markers. Surface-under-roof reconstruction is limited to SUP, received chunks, skylight and bounded scans; it is not a complete second Minecraft camera. Use beta38 clients and server with zonemap-3; server beta37 remains protocol-compatible. Core 2.1.2–2.x is server-only. Final corrected in-game tower rendering and full-modpack FPS/MSPT remain unverified.

Press M, pan/zoom and use YO to recenter. SUP supports the lower exterior surface; AUTO/Y CUEVA select cave layers. Keep your cache and let received areas refresh normally.

## Español

Minecraft 1.20.1, Forge 47.4.x, Java 17. ZoneCore 2.1.2–2.x es obligatorio solo para ZoneMap Server. Instala un JAR por lado; beta38 conserva zonemap-3.

Beta38 incorpora laterales con textura y superficie exterior comprobada bajo objetos flotantes. Corrige paredes ausentes bajo losas/escaleras, conserva transparencia, excluye bloques invisibles y mantiene fachadas visibles tras techos flotantes vecinos. Cambiar estilo renueva mosaicos recibidos; ZMT25 migra caché legible sin borrar marcadores. La superficie inferior se limita a SUP, chunks recibidos, luz de cielo y recorridos acotados; no es otra cámara completa. Usa cliente/servidor beta38 con zonemap-3; servidor beta37 sigue compatible por protocolo. Core 2.1.2–2.x solo en servidor. Faltan comprobación gráfica final de la torre corregida y mediciones FPS/MSPT del pack.

Pulsa M, desplaza/escala y usa YO para centrar. SUP admite superficie inferior exterior; AUTO/Y CUEVA seleccionan cuevas. Conserva caché y deja renovar las zonas recibidas.

## Updating / Actualizar

Stop the affected instance, back up world/configuration and replace only the previous same-mod/same-side JAR. Keep one JAR per mod per instance and preserve player data. / Detén la instancia correspondiente, respalda mundo/configuración y sustituye solo el JAR del mismo mod y lado. Conserva un JAR por mod e instancia y los datos de jugador.

## Validation scope / Alcance de verificación

Delivery probes cover tilted projection, partial side faces, lower surfaces, cache migration, water/color and bounded workers. The diagnostic image reconstructs old cache and is not a screenshot of the corrected final game. Full-modpack visual/performance checks remain pending.

Pruebas de entrega cubren proyección, caras parciales, superficie inferior, migración, colores/agua y trabajo acotado. La imagen de diagnóstico reconstruye caché antigua; no es captura del juego corregido. Sigue pendiente revisión visual/rendimiento del modpack.

## Rights / Derechos

Original ZONE code/assets © Elgochogms; existing third-party licenses and notices remain applicable. Public documentation repository. / Código y recursos originales ZONE © Elgochogms; se conservan licencias y avisos de terceros. Repositorio de documentación pública.


## Previous documentation / Documentación anterior

[2026-11-06 release / Entrega 2026-11-06](RELEASE-2026-11-06.md). Version examples in historical releases remain historical. / Los ejemplos de versiones de entregas anteriores son históricos.
