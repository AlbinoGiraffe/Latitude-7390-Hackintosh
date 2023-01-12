# Dell Latitude 7390 Hackintosh

Hackintosh files for Latitude 7390

Target Mac OS Version: Monterey (12.0)

## Hardware:

- Laptop Model: Latitude 7390 (081B)
- CPU Model: Core i5-8350U (Kaby Lake R)
- GPU Model: UHD Graphics 620
- Chipset: Dell Inc. 09386V A00
- Keyboard: AT Translated Set 2 Keyboard (PS/2)
- Touchpad: DELL081B:00 044E:120A Touchpad (I2C)
- Audio Codec: Realtek ALC3246 (ALC256)

  - 0x100002, layout 5, 11, 13, 14, 16, 17, 19, 20, 21, 22, 23, 24, 28, 33, 56, 57, 66, 67, 69, 70, 76, 77, 88, 97, 99

- Network Controller models
  - Wireless: Intel AC 8265 / 8275
  - Ethernet: Intel Ethernet I219-LM
- Storage: SAMSUNG MZFLV128HCGR-000MV (Upgraded to WDC WDS100T2B0C-00PXH0 with no changes needed)
- CFG Lock Offset: 0x52D

## Other steps needed:

- fix trackpad with SSDT-GPI0 and SSDT-XOSI
  - need to manually build and add patches
  - https://dortania.github.io/Getting-Started-With-ACPI/Laptops/trackpad.html
- Install Apple WiFi Card
  - Fenvi BCM94360NG
  - No kexts needed, native MacOS support
- Unlock CFG_Lock
  - Need to patch firmware

# Works

- Airdrop
- Unlock with Apple Watch
- Handoff
- iServices
- Sleep
- Trackpad and buttons (with gestures)
- Built-in keyboard
- Almost everything works

# Doesn't work

- Sidecar buggy
- Apple TV+ (DRM issue)
