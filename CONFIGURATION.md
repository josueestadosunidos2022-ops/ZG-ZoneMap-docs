# ZoneMap — Configuration / Configuración (2026-11-08)

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 1.0.0-beta38 |
| Client / Cliente | 1.0.0-beta38 |

## Beta38 terrain and cache / Terreno y caché beta38

No new TOML option is required. Preserve configurations, local/server markers and terrain cache. Beta38 writes ZMT25 and reads compatible older formats, marking received areas for refresh. Do not delete caches to update; keep a pre-update backup if a downgrade is planned. / No requiere opción nueva. Conserva configuraciones, marcadores y caché; ZMT25 lee formatos anteriores compatibles y renueva áreas recibidas. No borres caché para actualizar; respalda si prevés volver de versión.

The lower surface is only for SUP, not caves or Y SUP. It requires a skylit exterior gap within 16 blocks beneath the roof. At most 8192 extra reads per scan and a rotating starting point spread the work. Missing lighting or exhausted budget defers the area. It does not expose hidden rooms or invent missing ground. / Superficie inferior solo SUP; hueco exterior con luz de cielo dentro de 16 bloques, hasta 8192 lecturas adicionales por escaneo y comienzo rotativo. Falta de luz/presupuesto aplaza; no revela interiores ni inventa suelo.

Side rendering uses recorded visible south-face textures and alpha. Unreadable partial static models remain transparent for that row; cubic/dynamic models can use a material-color fallback. Up to eight side attempts per pixel limit transparent overlaps. Changing relief, contrast, textures or tint invalidates received tile style without waiting for the normal refresh. / Laterales usan textura y alfa registrados; parciales ilegibles no se convierten en cubos. Hasta ocho intentos por píxel; cambiar estilo renueva mosaicos recibidos.


## Client / Cliente

`config/zonemap-client.toml` contains local preferences. / Contiene preferencias locales.

| Key / Clave | Example / Ejemplo | Range or use / Rango o uso |
|---|---|---|
| `explorationChunksPerTick` | 6 | 1–12 newly received chunks / chunks nuevos recibidos |
| `scanBudgetMillis` | 4 | 1–12 ms; no new scan starts after budget / no inicia otro escaneo al agotarlo |
| `scanChunksPerTick` | 1 | 1–3 refreshes sharing the budget / renovaciones con presupuesto compartido |
| `maxTilesInMemory` | 2048 | Memory cache cap / Límite en memoria |
| `maxTilesOnDisk` | 30000 | Disk cache cap / Límite en disco |
| `adaptiveMapResolution` | true | Visible-size resolution, up to 768 px / Resolución adaptativa hasta 768 px |
| `largeMapTextureSize` | 384 | Fixed reference when adaptation disabled / Tamaño fijo sin adaptación |
| `tiltedMap` | true | False returns top-down view / False vuelve a vista cenital |
| `mapTiltDegrees` | 35 | 0–55 degrees / grados |
| `mapHeightScalePercent` | 100 | 25–150% |
| `maxHudMobIcons`, `maxEntityIcons` | 6 / 24 | HUD / large-map icon caps |
| `radarRangeBlocks` | 128 | Within client-known entities / Entre entidades conocidas por cliente |

If exploration stutters, try `scanBudgetMillis=2` and `explorationChunksPerTick=3`; new mapping can take longer. A single scan may exceed the time budget. / Si hay tirones, prueba 2 ms y 3 chunks; completar terreno puede tardar más. Un escaneo individual puede superar el presupuesto.

## Server / Servidor

Effective file: `<mundo>/serverconfig/zonemap-server.toml`; `defaultconfigs/zonemap-server.toml` is only a new-world template. / Archivo efectivo por mundo; defaultconfigs es plantilla para mundos nuevos.

| Key / Clave | Example / Ejemplo | Use / Uso |
|---|---|---|
| `syncPlayersPerTick` | 2 | 1–8 queued snapshots / vistas pendientes |
| `markerSyncSeconds` | 5 | 1–60 seconds / segundos |
| `protesRadiusChunks` | 12 | 2–16 chunks |
| `automaticMarkerDiscoveryRadiusChunks` | 8 | Nearby automatic discoveries / descubrimientos cercanos |
| `personalMarkerLimit` / `clanMarkerLimit` / `globalMarkerLimit` | 128 / 256 / 512 | Marker quotas / cuotas |

`allowCaveMap` and radar settings control shared rules. Optional integration toggles include `showZoneGuardianRegions`, `showActivatedWaystones`, `showDiscoveredZoneLevelUpArenas`, `showZoneProtesClaims`. Waystones uses each player's activated view, not every private stone. / Las reglas y toggles controlan funciones compartidas; Waystones usa la vista activada de cada jugador.

## Commands and data / Comandos y datos

```text
/zonemap marcador lista
/zonemap marcador personal crear <nombre>
/zonemap marcador clan crear <nombre>
/zonemap marcador global crear <nombre>
/zonemap marcador eliminar <uuid>
```

Global creation needs `zonemap.marker.global`; clan actions use membership/leadership permissions. No own teleport, pregeneration or reload command is added. / Global requiere permiso; clan requiere pertenencia/autorización. No añade teletransporte, pregeneración ni recarga propios.

Preserve `<mundo>/data/zonemap_markers.dat`, `zonemap/<hash>/<dimension>/` terrain cache and `config/zonemap/local-markers/<hash>.txt` local markers. Beta38 uses cache format ZMT25; earlier readable colors are shown flat until received chunks refresh heights and bases. Do not delete caches to update. Older versions cannot interpret ZMT25, so retain an old-cache backup if planning a downgrade. / Conserva datos y caché; colores antiguos legibles se muestran planos hasta actualizar alturas/bases. No borres caché para actualizar; guarda respaldo anterior si prevés volver de versión.

[Current release / Entrega actual](RELEASE-2026-11-08.md) · [README](README.md).
