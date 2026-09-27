# Projects

Public portfolio of systems built by Thompson (thompsonhome2013-alt).

## GhettoSystems (Android, v2.4.9)
- **Repo:** https://github.com/thompsonhome2013-alt/GhettoSystems
- **Stack:** Kotlin, Android, Retrofit-style API client
- **What it does:** Controls home lab devices — garage doors, power switches, device registry, biometric login, MCP server config, in-app assistant chat.
- **Key files:** `Gs2Api.kt` (API client), `DeviceRegistry.kt`, `BiometricLoginManager.kt`, `McpServersActivity.kt`

## GhettoSystems Ubuntu Cloud (backend)
- **Repo:** https://github.com/thompsonhome2013-alt/GhettoSystems-ubuntu-cloud
- **Stack:** PHP, MQTT, systemd services, LLM agent (RAG, tool use, SSH, vision)
- **What it does:** REST API v2 for device control and accounts; MQTT daemon; LLM agent with playbooks, scripts, and workspace tools; YouTube download service (ghetto-ytdl) writing to TrueNAS Jellyfin libraries; manufacturing admin UI.
- **Key paths:** `web/api/v2/`, `bin/gs2_mcp_bridge.py`, `systemd/`

## GhettoSystems UNO Q — GaragePLC (embedded + hardware)
- **Repo:** https://github.com/thompsonhome2013-alt/GhettoSystems-UNO-Q
- **Stack:** C++ (Arduino sketch), Python (RouterBridge agent), hardware design docs
- **What it does:** Firmware for an Arduino UNO Q controlling a garage door opener: pressure transducer on A5, head dump solenoid on D6, compressor on D7, WS2812 status on D3, app-settable cut-out pressure. Includes protohat schematic, BOM, and build notes.
- **Key paths:** `sketch/sketch.ino`, `python/main.py`, `hardware/protohat/`

## GhettoYT (Android, v3.0.4)
- **Repo:** https://github.com/thompsonhome2013-alt/GhettoYT
- **Stack:** Kotlin, Android
- **What it does:** YouTube/playlist downloader that pushes into TrueNAS Jellyfin libraries (Music, Music Videos, Movies, Kids). Job queue, cancel, file browser with rename, keyboard-aware UI.
- **Key files:** `MainActivity.kt`, `YtApi.kt`, `FilesActivity.kt`

## How I work
I use AI coding agents (Grok Build) as a build tool. I define the goal and architecture; the agent writes Makefiles, boilerplate, and first drafts; I review, correct, and ship. This is the same loop a tech lead uses with a junior engineer — direction, review, ownership.
