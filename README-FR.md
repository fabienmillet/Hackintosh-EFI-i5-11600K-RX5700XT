# Hackintosh EFI – i5-11600K + RX 5700 XT + Fenvi T919 (macOS Sequoia 15.5)

Ce dépôt contient le dossier EFI pour faire fonctionner **macOS Sequoia 15.5** sur un Hackintosh basé sur un processeur Intel Rocket Lake, une carte graphique AMD et une carte Fenvi T919 pour le Wi-Fi/Bluetooth natif Broadcom.

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

> SMBIOS : `iMacPro1,1`  
> OpenCore : `1.0.4`

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
-v debug=0x100 keepsyms=1 agdpmod=pikera npci=0x2000 wegtree=1
```

---

## 🖼️ Capture d’écran

![macOS Desktop](https://github.com/fabienmillet/Hackintosh-EFI-i5-11600K-RX5700XT/blob/main/screenshot.png?raw=true)

---

## ⚠️ Problèmes connus

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
* [Blackmagic Disk Speed Test](https://apps.apple.com/us/app/blackmagic-disk-speed-test/id425264550) (Crucial P3)
  * Lecture: 2944 MB/s
  * Ecriture: 1811 MB/s

---

## 📤 Mises à jour

- `(16-05-2024)` **Clone de l'OS du Crucial P3 vers mon WD Black SN850 (anciennement windows) pour permettre plus de performance** *(cela a en même temps mis à jour ma version de macos)*

---

## 📄 Remarques

- N’oubliez pas de générer vos propres numéros de série avec GenSMBIOS
- Testé avec OpenCore 1.0.4 + OpenCore Legacy Patcher (patch Wi-Fi uniquement)
- Installation propre de macOS Sequoia 15.5
