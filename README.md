# Dell OptiPlex 3050 – macOS Tahoe Workstation (EFI)

## Overview
This project transforms the Dell OptiPlex 3050 into a stable, efficient macOS Tahoe workstation using a custom EFI configuration.  
It is designed for sustainability, performance optimization, and accessible entry into the Apple ecosystem without requiring official Apple hardware upgrades.


<img width="1920" height="1080" alt="Screenshot 2026-04-06 at 13 39 27" src="https://github.com/user-attachments/assets/7f772db1-9192-44f9-8dae-69159822794e" />

---

## Why Repurpose?

### 🌱 Sustainability First
Enterprise desktops are often retired prematurely due to warranty cycles rather than actual performance limits.  
The Intel Kaby Lake platform in the OptiPlex 3050 remains capable of modern workloads.  
Repurposing reduces electronic waste and extends hardware lifecycle value.

### ⚡ Efficiency Gains
Compared to modern resource-heavy operating systems, macOS provides a streamlined UNIX-based environment with lower background overhead.  
On this hardware, system responsiveness is optimized for workflow-focused computing.

### 💻 Development Access
This setup enables access to macOS-exclusive tools such as:
- Xcode
- Final Cut Pro
- Logic Pro

It provides a cost-effective development environment for Apple ecosystem applications.

### 🏡 Home / Lab Use
The OptiPlex 3050 form factor and low power consumption make it suitable for:
- Media servers (Plex / Jellyfin)
- Time Machine backups
- Lightweight home automation services

### 🔒 Privacy-Oriented Computing
macOS offers strong privacy controls, including on-device processing and reduced telemetry compared to many mainstream consumer operating systems.

---

## Hardware Target
- Dell OptiPlex 3050
- Intel 7th Gen Kaby Lake CPU
- Integrated Intel HD Graphics
- Standard enterprise SFF configuration

---

## macOS Version Tested
- macOS Tahoe 26.4.1 (25E253)

---

## Installation Notes
- EFI is configured for stable boot on supported hardware.
- Ensure BIOS settings are optimized for macOS compatibility (UEFI mode, disabled secure boot where required).

### Important Patch Requirement
To ensure full audio functionality:

> Use **MyKextInstaller** to patch `AppleHDA.kext`  
https://github.com/Mirone/MyKextInstaller/releases/tag/1.8

---

## Tested Status
This EFI has been validated on Dell OptiPlex 3050 hardware and confirmed to deliver stable operation across all primary system components under macOS Tahoe 26.4 (25E246).

---

## Disclaimer
This project is intended for educational and research purposes.  
Users are responsible for ensuring compliance with their local software and hardware usage policies.

---

## Status
Stable Build – Production Ready for Supported Hardware
