# Hackintosh EFI – i5-11600K + RX 5700 XT + Fenvi T919 (macOS Tahoe 26.2)

Ce dépôt contient le dossier EFI pour faire fonctionner **macOS Tahoe 26.2** sur un Hackintosh basé sur un processeur Intel Rocket Lake, une carte graphique AMD et une carte Fenvi T919 pour le Wi-Fi/Bluetooth natif Broadcom.

---

## 💻 Spécifications matérielles

| Composant         | Modèle                                     |
|-------------------|--------------------------------------------|
| Carte mère        | ASUS PRIME B560M-A                         |
| Processeur        | Intel Core i5-11600K (11ᵉ gén.)            |
| Carte graphique   | AMD Radeon RX 5700 XT                      |
| RAM               | 32 Go DDR4 2666 MHz                        |
| SSD              | WD Black SN850 500GB (WDS500G1XHE-00AFY0)   |
| Wi-Fi/Bluetooth   | Fenvi T919 (BCM94360CD)                    |
| Ethernet          | Intel I219V-14                             |

> SMBIOS : `MacPro7,1`  
> OpenCore : `1.0.6`

---

## ✅ Fonctionnalités prises en charge

- Accélération graphique complète (RX 5700 XT)
- AirDrop, Handoff, Presse-papiers universel
- Wi-Fi + Bluetooth (Fenvi T919)
- App Store, iMessage, FaceTime
- Ethernet opérationnel

---

## 📦 SSDT utilisés (ACPI)

- `SSDT-EC.aml`
- `SSDT-PLUG.aml`
- `SSDT-RTCAWAC.aml`
- `SSDT-SBUS.aml`
- `SSDT-USB-Reset.aml`
- `SSDT-USBX.aml`

Générés avec SSDTTime et adaptés à un système Rocket Lake.

---

## 🧩 Kexts utilisés

- Lilu  
- WhateverGreen  
- VirtualSMC  
- AppleALC  
- IntelMausi   
- AMFIPass  
- IO80211FamilyLegacy  
- IOSkywalkFamily  
- RestrictEvents  
- SMCProcessor  
- SMCSuperIO 
- XHCI-unsupported

---

## ⚙️ Arguments de démarrage (boot-args)

```
debug=0x100 keepsyms=1 -amfipassbeta
```

---

## 🖼️ Capture d’écran

![macOS Desktop](https://github.com/fabienmillet/Hackintosh-EFI-i5-11600K-RX5700XT/blob/main/screenshot.png?raw=true)

---

## ⚠️ Problèmes connus

- Patch OCLP sur 26.2
- Aucun pour l’instant. Système stable depuis le passage de la HB-1200 (défectueuse) à la T919.

---

## 🚀 Benchmarks

* [Geekbench 6.4](https://www.geekbench.com/)
  * Un seul coeur: 1956
  * Multi-Coeur: 8179
  * OpenCL: 64987
  * Metal: 108540
* [Cinebench 2024.1.0](https://www.maxon.net/en/cinebench)
  * Un seul coeur: 95
  * Multi-Coeur: 614
  * GPU: 3352
* [Blackmagic Disk Speed Test](https://apps.apple.com/us/app/blackmagic-disk-speed-test/id425264550) (WD Black SN850)
  * Lecture: 5598 MB/s
  * Ecriture: 4264 MB/s

---

## 📤 Mises à jour

- `(01-02-2026)` **Mise à jour vers macOS Tahoe 26.2**
- `(24-05-2025)` **Ajout de OpenLinuxBoot.efi pour permettre de boot sur Linux en multi-boot**
- `(16-05-2025)` **Clone de l'OS du Crucial P3 vers mon WD Black SN850 (anciennement windows) pour permettre plus de performance** *(cela a en même temps mis à jour ma version de macos)*

---

## 📄 Remarques

- N’oubliez pas de générer vos propres numéros de série avec GenSMBIOS
- Testé avec OpenCore 1.0.6 + OpenCore Legacy Patcher (patch Wi-Fi uniquement)
- Installation propre de macOS Tahoe 26.2
