# ZG ZoneMap

## Update / Actualización — 2026-10-17

Selected version / Versión seleccionada: **server 1.0.0-beta11 / client 1.0.0-beta11**. New file availability depends on CurseForge approval / La disponibilidad de los archivos nuevos depende de su aprobación en CurseForge.

See [changes, exact files and installation](UPDATES-2026-10-17.md) / Consulta [cambios, archivos e instalación](UPDATES-2026-10-17.md). Preserve the world and TOML files / Conserva mundo y TOML.

## English

RPG world and cave map with HUD, radar, local tile cache and synchronized markers. Minecraft 1.20.1 / Forge 47.x. Current protected pair: **Server + Client 1.0.0-beta11** in one CurseForge project.

### Installation

Install the labeled server JAR on the server and client JAR on players' clients. Never place both in one `mods` folder. The server requires **ZoneCore 2.1.2+**; the client does not. ZoneLevelUp beta29-r10, ZoneGuardian, ZoneProtes, ZoneClans and Waystones integrations are optional. ZoneProtes itself needs its own matching client/server pair when installed.

### Configuration

Edit generated TOML files while the server or game is stopped unless a documented reload command is available. Back up persistent data before updates.

| Config file | Use |
|---|---|
| `zonemap-client.toml` | Verify the exact generated path and options for the selected release. |
| `zonemap-server.toml` | Verify the exact generated path and options for the selected release. |

See [configuration reference](CONFIGURATION.md) for keys detected in source and [release compatibility](RELEASES.md) for version-pair rules.

## Español

Mapa RPG de superficie y cuevas con HUD, radar, caché de teselas y marcadores sincronizados. Minecraft 1.20.1 / Forge 47.x. Pareja protegida actual: **Server + Client 1.0.0-beta11** en un proyecto CurseForge.

### Instalación

Instala el JAR servidor en el servidor y el cliente en los jugadores. Nunca pongas ambos en la misma carpeta `mods`. El servidor requiere **ZoneCore 2.1.2+**; el cliente no. Las integraciones con ZoneLevelUp beta29-r10, ZoneGuardian, ZoneProtes, ZoneClans y Waystones son opcionales. ZoneProtes exige su propia pareja cliente/servidor cuando se instala.

### Configuración

Edita los TOML generados con el servidor o juego detenido, salvo que exista un comando de recarga documentado. Respalda los datos persistentes antes de actualizar.

| Archivo de configuración | Uso |
|---|---|
| `zonemap-client.toml` | Comprueba la ruta y opciones generadas de la entrega elegida. |
| `zonemap-server.toml` | Comprueba la ruta y opciones generadas de la entrega elegida. |

Consulta la [referencia de configuración](CONFIGURATION.md) para claves detectadas en el código y la [compatibilidad de entregas](RELEASES.md) para las parejas de versiones.

## Ownership / Titularidad

Documentation and original ZONE visual assets © Elgochogms. This repository contains documentation and a project avatar only; it does not distribute mod source code, private mappings, server secrets or production configuration.

