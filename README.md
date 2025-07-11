# 🍏 macOS 15.5 Sequoia Hackintosh – Fenvi T919 Build  
![macOS](https://img.shields.io/badge/macOS-15.5_Sequoia-blue.svg)
![Fenvi T919](https://img.shields.io/badge/WiFi-Bluetooth_Ready-green.svg)
![OpenCore](https://img.shields.io/badge/OpenCore-1.0.4-brightgreen.svg)
![Status](https://img.shields.io/badge/Build-Stable-success.svg)

> 🛠️ Hackintosh config with full wireless support using **Fenvi T919**  
> 📦 Comes with `ShowPicker = true` & `HideAuxiliary = false` for easier setup  
> ✅ Wireless, Bluetooth, Audio, and Graphics acceleration working flawlessly on macOS 15.5


![Screenshot 2025-06-22 at 06 46 41](https://github.com/user-attachments/assets/3234014e-d747-4606-b173-fd38e82822d0)



---

## 🚀 Post-Install Instructions

### 🔧 Step 1: Disable SIP (System Integrity Protection)
- Boot into **macOS Recovery** using the OpenCore Picker (`ShowPicker = true`, `HideAuxiliary = false`)
- From the top menu, open `Utilities > Terminal`

```bash
csrutil disable
```

- Restart back into macOS

---

### 🛠️ Step 2: Apply Root Patches with OCLP
1. Open **OpenCore Legacy Patcher (OCLP)** from `/Applications`
2. Run **Post-Install Root Patch**
3. Ensure **Modern Wireless Patch** is selected (required for Fenvi T919)
4. Reboot when done

---

### 🧹 Optional Cleanup (after successful wireless patch)
Edit `config.plist` using [ProperTree](https://github.com/corpnewt/ProperTree) or OpenCore Configurator:

| Setting                | Path                             | Final Value |
|------------------------|----------------------------------|-------------|
| OpenCore Boot Picker   | Misc > Boot > ShowPicker         | `false`     |
| Hide Auxiliary Entries | Misc > Boot > HideAuxiliary      | `true`      |

---

## 🧪 Tested Configuration (Verified Working Build)

| Component            | Specification                                     |
|----------------------|---------------------------------------------------|
| **macOS Version**    | macOS Sequoia 15.5 (24F74)                        |
| **Model Identifier** | iMac20,2 (27-inch Retina 5K, 2020) via SMBIOS     |
| **CPU**              | Intel Core i3-7100 @ 3.90GHz (Kaby Lake)          |
| **Cores / Threads**  | 2 Cores / 4 Threads                               |
| **RAM**              | 8GB DDR4 2400MHz                                  |
| **Storage**          | Kingston SATA SSD 240GB (Apple SSD - Startup Disk)|
| **Graphics**         | Intel HD Graphics 630 (1536MB)                    |
| **Display**          | HDMI & Display Port                               |
| **Graphics Accel.**  | ✅ Metal 3 Supported / VDA Fully Accelerated      |
| **Wireless + BT**    | Fenvi T919 (Broadcom BCM94360CD) – Native Support |
| **Audio Codecs**     | Realtek ALC255, Intel HDA                         |
| **Bootloader**       | OpenCore 1.0.4 (Release Build)                    |

---

## 🧩 Verified PCI Devices (Vendor Breakdown)

| Vendor               | Device Name                                                             | Class                   | Subclass                |
|----------------------|------------------------------------------------------------------------|-------------------------|-------------------------|
| **Intel Corporation**| Xeon E3-1200 v6/7th Gen Core Processor Host Bridge/DRAM Registers       | Bridge                  | Host bridge             |
| **Intel Corporation**| Intel HD Graphics 630                                                  | Display controller      | VGA compatible controller |
| **Intel Corporation**| 200 Series/Z370 USB 3.0 xHCI Controller                                | Serial bus controller   | USB controller          |
| **Intel Corporation**| 200 Series PCH Thermal Subsystem                                       | Signal processing       | Signal processing       |
| **Intel Corporation**| 200 Series PCH CSME HECI #1                                            | Communication controller| Communication controller|
| **Intel Corporation**| 200 Series PCH SATA Controller [AHCI mode]                             | Mass storage controller | SATA controller         |
| **Intel Corporation**| 200 Series PCH PCI Express Root Port #5                                | Bridge                  | PCI bridge              |
| **Intel Corporation**| 200 Series PCH PCI Express Root Port #7                                | Bridge                  | PCI bridge              |
| **Intel Corporation**| 200 Series PCH LPC Controller (B250)                                   | Bridge                  | ISA bridge              |
| **Intel Corporation**| 200 Series/Z370 Power Management Controller                            | Memory controller       | Memory controller       |
| **Intel Corporation**| 200 Series PCH HD Audio                                               | Multimedia controller   | Audio device            |
| **Intel Corporation**| 200 Series/Z370 SMBus Controller                                      | Serial bus controller   | SMBus                   |
| **Realtek**          | RTL8111/8168/8411 PCIe Gigabit Ethernet                               | Network controller      | Ethernet controller     |
| **Broadcom Inc.**    | BCM4360 802.11ac Dual Band Wireless Adapter (Fenvi T919)               | Network controller      | Wireless adapter        |

---

## 🔧 Recommended Kexts

| Kext                   | Purpose                         | Required |
|------------------------|----------------------------------|----------|
| `Lilu.kext`            | Core patching engine             | ✅        |
| `WhateverGreen.kext`   | iGPU acceleration + framebuffer  | ✅        |
| `AppleALC.kext`        | Audio codec patching             | ✅        |
| `RealtekRTL8111.kext`  | Ethernet                         | ✅        |
| `VirtualSMC.kext`      | Power management & sensors       | ✅        |
| `SMCBatteryManager.kext` | Battery status (laptops only) | ❌        |

---

## 🗣️ Sprachunterstützung / Language Support

If you're a German-speaking user:
- Du kannst mir gerne eine Nachricht schicken, wenn du Hilfe beim Setup brauchst.
- README in Deutsch kommt bald. 🙌

---

## 💬 Support & Resources

- 🔗 [OpenCore Legacy Patcher (OCLP)](https://github.com/dortania/OpenCore-Legacy-Patcher)
- 📖 [OpenCore Vanilla Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- 🗨️ [Join Dortania on Discord](https://discord.gg/oclp)

---

## 🌟 Contribute

If this build worked for you:
- Leave a ⭐ on this repo  
- Fork it  
- Contribute fixes, add BIOS settings, USB maps, etc.

---

## 🔐 Disclaimer

This EFI and configuration is for educational and testing purposes only.  
Ensure you are using macOS legally and ethically.  
Hackintosh at your own risk.
