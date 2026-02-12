# esp-srmodels

Pre-built ESP-SR speech recognition model partition images for [Willow](https://github.com/HeyWillow/willow) devices.

## What is this?

This repository provides ready-to-flash `srmodels.bin` files for Willow's OTA model update feature. Each release contains individual wake word model partition images built from [Espressif's ESP-SR](https://github.com/espressif/esp-sr) repository.

## Downloads

Check the [Releases](https://github.com/HeyWillow/esp-srmodels/releases) page for pre-built model tarballs.

Each tarball contains:
- `srmodels.bin` — packed model partition image (flash via Willow OTA)
- `LICENSE` — MIT license from ESP-SR
- `SOURCE.txt` — link to the original model source

## How it works

A GitHub Actions workflow:
1. Clones the ESP-SR repository
2. Packs each WakeNet v9 (`wn9_*`) model using Espressif's `pack_model.py`
3. Creates tarballs with license attribution
4. Publishes as a GitHub Release

## License

The wake word models are from [Espressif's ESP-SR](https://github.com/espressif/esp-sr) and are licensed under the [MIT License](https://github.com/espressif/esp-sr/blob/master/LICENSE).
