# Hackintosh EFI – i5-11600K + RX 5700 XT + Fenvi T919 (macOS Tahoe 26.2)

This repository contains a fully functional EFI folder for running **macOS Tahoe 26.2** on a Hackintosh system based on an Intel Rocket Lake CPU, AMD GPU, and native Broadcom Wi-Fi/Bluetooth support using a Fenvi T919 card.

---

## 💻 Hardware Specifications

| Component        | Model                                       |
|------------------|---------------------------------------------|
| Motherboard      | ASUS PRIME B560M-A                          |
| CPU              | Intel Core i5-11600K (11th Gen)             |
| GPU              | AMD Radeon RX 5700 XT                       |
| RAM              | 32GB DDR4 2666 MHz                          |
| SSD              | WD Black SN850 500GB (WDS500G1XHE-00AFY0)   |
| Wi-Fi/Bluetooth  | Fenvi T919 (BCM94360CD)                     |
| Ethernet         | Intel I219V-14                              |

> SMBIOS: `MacPro7,1`  
> OpenCore version: `1.0.6`

---

## ✅ Functional Features

- Full graphics acceleration (RX 5700 XT)
- AirDrop, Handoff, Universal Clipboard
- Wi-Fi + Bluetooth (Broadcom via Fenvi T919)
- App Store, iMessage, FaceTime
- Ethernet working

---

## 📦 ACPI SSDTs Used

- `SSDT-EC.aml`
- `SSDT-PLUG.aml`
- `SSDT-RTCAWAC.aml`
- `SSDT-SBUS.aml`
- `SSDT-USB-Reset.aml`
- `SSDT-USBX.aml`

These SSDTs were generated with SSDTTime and adapted for a Rocket Lake setup.

---

## 🧩 Kexts Included

- Lilu
- WhateverGreen
- VirtualSMC
- AppleALC
- IntelMausi
- USBMap
- AMFIPass
- IO80211FamilyLegacy
- IOSkywalkFamily
- RestrictEvents
- SMCProcessor
- SMCSuperIO
- XHCI-unsupported

---

## ⚙️ Boot Arguments

```
debug=0x100 keepsyms=1 -amfipassbeta
```

---

## 🖼️ Screenshot

![macOS Desktop](https://github.com/fabienmillet/Hackintosh-EFI-i5-11600K-RX5700XT/blob/main/screenshot.png?raw=true)

---

## ⚠️ Known Issues

Patch OCLP on 26.2

---

## 🚀 Benchmarks

* [Geekbench 6.4](https://www.geekbench.com/)
  * Single Core: 1956
  * Multicore: 8179
  * OpenCL: 64987
  * Metal: 108540
* [Cinebench 2024.1.0](https://www.maxon.net/en/cinebench)
  * Single Core: 95
  * Multicore: 614
  * GPU: 3352
* [Blackmagic Disk Speed Test](https://apps.apple.com/us/app/blackmagic-disk-speed-test/id425264550) (WD Black SN850)
  * Read: 5598 MB/s
  * Write: 4264 MB/s

---

## 📤 Upgrades

- `(01-02-2026)` **Updated to macOS Tahoe 26.2**
- `(24-05-2025)` **Add OpenLinuxBoot.efi to enable multi-boot booting on Linux**
- `(16-05-2025)` **OS clone from the Crucial P3 to my WD Black SN850 (formerly windows) for better performance** *(it also updated my macos version)*

---

## 📝 Notes

- Don't forget to generate your own serial numbers using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
- Built with OpenCore 1.0.6 and OpenCore Legacy Patcher (Wi-Fi patch only)
- Clean install of macOS Tahoe 26.2
