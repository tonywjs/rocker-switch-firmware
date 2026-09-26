# rocker-switch-firmware

Signed firmware images for a personal ESP32-C3 device that presses a wall light switch.

- Each release `vN` contains `firmware.bin` and `manifest.json` (`{"version": N, "tag": "vN", "asset": "firmware.bin"}`).
- Devices check `releases/latest/download/manifest.json` once a day and install a higher version.
- Images are signed with an RSA-3072 key (ESP-IDF Secure Boot V2 scheme, signed-app verification without secure boot). Devices reject images that are unsigned or signed with any other key, so this repository is only a delivery channel.
- No source code, Wi-Fi credentials, device tokens or HomeKit codes are stored here; those live on each device.
