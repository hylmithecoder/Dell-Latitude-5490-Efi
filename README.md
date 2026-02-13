# Dell Latitude 5490 Hackintosh (OpenCore)

This repository contains the OpenCore EFI configuration for running macOS on a Dell Latitude 5490.

## Hardware Specifications

*   **Laptop Model:** Dell Latitude 5490
*   **Processor:** Intel Core i5-7300U (Kaby Lake)
*   **Graphics:** Intel HD Graphics 620
*   **Audio:** Realtek ALC3246 (ALC256)
*   **Wi-Fi:** Intel Dual Band Wireless-AC 8265
*   **Bluetooth:** Intel Bluetooth
*   **Ethernet:** Intel I219-LM

## Working Features

Based on the kexts included and user feedback, the following features are working:

*   **Wi-Fi:** Working (Intel Wireless)
*   **Bluetooth:** Working (Intel Bluetooth)
*   **Audio:** Working (Internal Speakers & Headphone Jack)
*   **Graphics Acceleration:** Working (Intel HD 620)
*   **Trackpad & Keyboard:** Working (PS2 & I2C)
*   **Battery Status:** Working
*   **Brightness Control:** Working (Using `BrightnessKeys.kext`)
*   **Ethernet:** Working
*   **USB Ports:** Working

## Kexts Included

The following kexts are included in the EFI configuration:

*   **VirtualSMC.kext:** Essential SMC emulator.
*   **Lilu.kext:** Arbitrary kext, library, and program patching.
*   **WhateverGreen.kext:** Graphics fixing.
*   **AppleALC.kext:** Native macOS audio support.
*   **AirportItlwm.kext:** Intel Wi-Fi support.
*   **IntelBluetoothFirmware.kext / IntelBTPatcher.kext / BlueToolFixup.kext:** Intel Bluetooth support.
*   **VoodooPS2Controller.kext:** PS/2 keyboard/mouse/trackpad support.
*   **VoodooI2C.kext / VoodooI2CHID.kext:** I2C trackpad support.
*   **BrightnessKeys.kext:** Brightness key support.
*   **SMCBatteryManager.kext / SMCLightSensor.kext / SMCProcessor.kext:** Battery, ambient light sensor, and processor monitoring.
*   **IntelMausi.kext:** Intel Ethernet support.
*   **RealtekRTL8111.kext:** Realtek Ethernet support.
*   **AtherosE2200Ethernet.kext:** Atheros Ethernet support.
*   **USBInjectAll.kext / XHCI-unsupported.kext:** USB port mapping and support.
*   **NVMeFix.kext:** NVMe power management improvements.
*   **ECEnabler.kext:** Fixes battery status on many laptops.
*   **RestrictEvents.kext:** Block unwanted processes.

## Installation

1.  **Format USB:** Create a bootable macOS installer USB.
2.  **Mount EFI:** Mount the EFI partition of your USB drive.
3.  **Copy EFI:** Copy the `EFI` folder from this repository to the EFI partition of your USB drive.
4.  **BIOS Settings:** Ensure BIOS settings are optimized for macOS (Disable Secure Boot, VT-d, Fast Boot, etc.).
5.  **Install:** Boot from the USB and install macOS.

## Credits

*   [OpenCore](https://github.com/acidanthera/OpenCorePkg)
*   [Acidanthera](https://github.com/acidanthera) for Lilu, WhateverGreen, AppleALC, and many other essential kexts.
*   The Hackintosh Community for their guides and support.
