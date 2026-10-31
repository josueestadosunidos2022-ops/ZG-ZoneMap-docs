# ZoneMap 1.0.0-beta31

## English

RPG map, cave views, radar and persistent shared markers. Beta31 removes surface overlays from cave views, rejects old cave tiles until rescanned, and uses ZMT16 without deleting surface maps or markers. Both file metadata and manifests identify beta31; network protocol remains zonemap-3. Keep caches and markers; old cave tiles rebuild from received chunks.

## Español

Mapa RPG, vistas de cuevas, radar y marcadores persistentes. Beta31 elimina referencias de superficie en cuevas y rechaza mosaicos antiguos hasta volver a escanearlos; utiliza ZMT16 y conserva superficie y marcadores. Se corrigió el número beta30 heredado en los metadatos de ambos JAR para identificar beta31. El protocolo sigue siendo zonemap-3.


| Side / Lado | Version | File |
|---|---|---|
| server | 1.0.0-beta31 | `zonemap-server-1.0.0-beta31-protected.jar` |
| client | 1.0.0-beta31 | `zonemap-client-1.0.0-beta31-protected.jar` |

## Dependencies / Dependencias

- **server**: zonecore: Required Dependency ([2.1.2,3))
- **client**: No additional mod requirement / Sin requisitos adicionales

## Installation / Instalación

Install only the file for each side. Never mix two versions or both side distributions in one mods folder. Back up the world and preserve TOML/player data. Dedicated-server-only mods do not belong in a client modpack.

Instala solo el archivo del lado correspondiente. No mezcles versiones ni ambos JAR en una carpeta mods. Respalda mundo y conserva TOML/progreso. Los mods exclusivos de servidor no van en el modpack de cliente.

Protected public files retain features without distributing private source, mappings or production configuration/account data. File/resources/shared schemas and isolated server startup/clean save were checked; no new GUI/full-modpack or live multiplayer test was performed. File availability depends on CurseForge approval.

Los archivos públicos conservan funciones con protección, sin fuentes, mappings ni datos privados. Se verificaron archivos/esquemas y arranque/cierre local aislado; no una nueva prueba gráfica o multijugador real. Disponibilidad sujeta a aprobación de CurseForge.

## Ownership / Titularidad

Original ZONE code and artwork © Elgochogms. All Rights Reserved. Public documentation repository only; source and mappings remain private.
