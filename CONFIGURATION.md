# ZoneMap — Configuration / Configuración (2026-11-06)

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 1.0.0-beta36 |
| Client / Cliente | 1.0.0-beta36 |

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

If exploration stutters, try `scanBudgetMillis=2` and `explorationChunksPerTick=3`; new mapping can take longer. A single scan may exceed the time budget. / Si hay tirones, prueba 2 ms y3 chunks; completar terreno puede tardar más. Un escaneo individual puede superar el presupuesto.

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

Preserve `<mundo>/data/zonemap_markers.dat`, `zonemap/<hash>/<dimension>/` terrain cache and `config/zonemap/local-markers/<hash>.txt` local markers. Beta36 uses cache format ZMT23; earlier readable colors are shown flat until received chunks refresh heights and bases. Do not delete caches to update. Older versions cannot interpret ZMT23, so retain an old-cache backup if planning a downgrade. / Conserva datos y caché; colores antiguos legibles se muestran planos hasta actualizar alturas/bases. No borres caché para actualizar; guarda respaldo anterior si prevés volver de versión.

[Current release / Entrega actual](RELEASE-2026-11-06.md) · [README](README.md).
