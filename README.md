# PD48V

Projektseite und Firmware-Flasher für das PD48V, ein 240-W-Labornetzteil mit USB-C-PD-3.1-Eingang.

**Seite:** GitHub Pages dieses Repositorys (`index.html`).

## Firmware flashen

Seite in Chrome oder Edge am Computer öffnen, Gerät per USB-C anschließen, passenden Knopf drücken:

| Knopf | Modul | Dateien |
|---|---|---|
| Board mit PSRAM | ESP32-S3 N16R8 / S3R8 | `fw/board-psram/` |
| Board ohne PSRAM | ESP32-S3-WROOM-1-N16 | `fw/board-n16/` |
| WLAN-Dongle | ESP32-C3 | `fw/dongle-c3/` |

Offsets stehen in `manifest-*.json` (ESP Web Tools). Board: 0x0 Bootloader, 0x8000 Partitionen, 0x10000 OTA-Daten, 0x20000 App. Dongle: 0x0, 0x8000, 0x10000. Der NVS-Bereich (0x9000) wird nicht überschrieben, Einstellungen bleiben erhalten.

Firmware-Stand: 2026-11-20.
