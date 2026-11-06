# ZoneMap

A client minimap and world map with terrain layers, radar, personal/clan/global markers and optional server integrations.

Minimapa y mapa grande de cliente con capas de terreno, radar, marcadores personales/de clan/globales e integraciones opcionales.

## Current release / Entrega actual — 2026-11-06

Minecraft **1.20.1**, Forge **47.x** (47.4.x for this release set), Java **17**. File availability follows CurseForge approval. / Disponibilidad de archivos según aprobación de CurseForge.

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 1.0.0-beta36 |
| Client / Cliente | 1.0.0-beta36 |

**Protocol / Protocolo:** zonemap-3.

[Downloads / Descargas](https://www.curseforge.com/projects/1738053/files) · [Release guide / Guía de novedades](RELEASE-2026-11-06.md) · [Configuration / Configuración](CONFIGURATION.md)

## English — Requirements and quick start

Server: ZoneCore 2.1.2+ below 3. The client does not require Core. Clan, protection, region, arena and waystone integrations need their corresponding installed modules. Use the beta36 pair for all improvements.

Press M, drag to pan, scroll to zoom and use YO to recenter. Choose SUP/AUTO/Y layers, create a permitted marker and use SEGUIR for guidance. DISEÑO Y MINIMAPA controls icon, color, HUD size and style.

### What changed

- Reorganized controls and marker search/scroll, custom shaded symbols and clearer water/terrain colors.
- Tilted terrain uses recorded heights and checked physical side bases; markers, radar and protection borders share the projection.
- Bounded background composition, prioritized received-chunk scanning and grouped server marker/protection synchronization.

## Español — Requisitos e inicio

Servidor: ZoneCore 2.1.2+ menor que 3. El cliente no exige Core. Integraciones de clan, protecciones, regiones, arenas y waystones requieren sus módulos. Usa la pareja beta36 para todas las mejoras.

Pulsa M, arrastra, usa rueda para escala y YO para centrar. Elige capas SUP/AUTO/Y, crea un marcador permitido y SEGUIR para guiarte. DISEÑO Y MINIMAPA controla icono, color, tamaño y estilo.

### Novedades

- Controles reorganizados, búsqueda/scroll de marcadores, símbolos sombreados y colores de agua/terreno más claros.
- Terreno inclinado con alturas y bases físicas comprobadas; marcadores, radar y bordes comparten proyección.
- Composición acotada en segundo plano, exploración prioritaria de chunks recibidos y sincronización agrupada de datos del servidor.

## Updating / Actualizar

Stop the affected instance, back up world/configuration, replace only the previous same-mod/same-side JAR and retain player data. Never install the dedicated and client JARs of one mod together. / Detén la instancia correspondiente, respalda mundo/configuración y sustituye solo el JAR del mismo mod y lado conservando datos. Nunca instales juntos los JAR dedicado y cliente del mismo mod.

## Validation scope / Alcance de verificación

Delivery checks cover marker audiences/quotas/persistence and tilted projection/physical faces. Cache previews are not screenshots of the final game geometry. Full multiplayer modpack and FPS/MSPT measurements are not established by these checks.

Las comprobaciones cubren audiencia/cuotas/persistencia de marcadores y proyección/caras físicas. Previews de caché no son capturas de geometría final del juego. No certifican modpack multijugador ni mediciones FPS/MSPT.

## Rights / Derechos

Original ZONE code and assets © Elgochogms; existing licenses and third-party notices remain applicable. This repository provides public documentation. / Código y recursos originales ZONE © Elgochogms; se conservan licencias y avisos de terceros. Este repositorio contiene documentación pública.
