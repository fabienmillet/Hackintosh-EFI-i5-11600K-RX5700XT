# Hackintosh EFI – i5-11600K + RX 5700 XT + Fenvi T919 (macOS Sequoia 15.4.1)

This repository contains a fully functional EFI folder for running **macOS Sequoia 15.4.1** on a Hackintosh system based on an Intel Rocket Lake CPU, AMD GPU, and native Broadcom Wi-Fi/Bluetooth support using a Fenvi T919 card.

---

## 💻 Hardware Specifications

| Component        | Model                            |
|------------------|----------------------------------|
| Motherboard      | ASUS PRIME B560M-A               |
| CPU              | Intel Core i5-11600K (11th Gen)  |
| GPU              | AMD Radeon RX 5700 XT            |
| RAM              | 32GB DDR4 2666 MHz               |
| SSD              | Crucial P3 500GB (CT500P3SSD8)   |
| Wi-Fi/Bluetooth  | Fenvi T919 (BCM94360CD)          |
| Ethernet         | Intel I219V-14                   |

> SMBIOS: `iMacPro1,1`  
> OpenCore version: `1.0.4`

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
-v debug=0x100 keepsyms=1 agdpmod=pikera npci=0x2000 wegtree=1
```

---

## 🖼️ Screenshot

![macOS Desktop](https://github.com/fabienmillet/Hackintosh-EFI-i5-11600K-RX5700XT/blob/main/screenshot.jpg?raw=true)

---

## ⚠️ Known Issues

None at the moment. Stable since switching from a faulty Fenvi HB-1200 to the T919.

---

## 📝 Notes

- Built with OpenCore 1.0.4 and OpenCore Legacy Patcher (Wi-Fi patch only)
- Clean install of macOS Sequoia 15.4.1
