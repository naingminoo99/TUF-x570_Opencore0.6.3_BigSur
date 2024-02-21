# TUF X570 Hackintosh Guide
#### Big Sur with Everything Working (Apple Services, Sleep)
[![N|Solid](https://d2.alternativeto.net/dist/icons/opencore_168788.png?width=64&height=64&mode=crop&upscale=false)](https://github.com/dortania/OpenCore-Install-Guide)

This guide focuses solely on the Asus TUF X570 Plus. While the provided EFI may work on similar systems, I do not recommend using it without proper adjustments.
- Tips
  - Avoid using configurators (most tools out there are Clover-only supported).
  - Refrain from following YouTube guides; instead, refer to the Dortania Guide for stability.
  - Avoid copying other people's EFI; although it might boot, it can lead to problems later on.
  - Enjoy the process of doing it yourself; understanding what makes your hackintosh will aid in maintenance and troubleshooting.
  - Read the Dortania Guide thoroughly, multiple times.
  - Be persistent and keep trying until successful.

### Specifications

- Motherboard: Asus TUF X570
- CPU: Ryzen 7 3700X
- GPU: ROG Strix Radeon RX Vega 64 8GB
- PSU: Superflower 850W 80+ Gold
- RAM: 3200MHz 32GB (2x16)
- NVMe1: 500GB
- NVMe2: 500GB
- Chassis: Corsair iCUE 465x
- AIO: Corsair H100i RGB
- Fans: Corsair LL120 RGB
- Network: Fenvi FV-T919

[PC Part Picker Link](https://pcpartpicker.com/list/43drvf)

### Rig
I named this rig "Ryzenshine" since it's all AMD, plus it shines!

![RyzenshinePic](https://i.imgur.com/h6qTf1I.jpg)

### BIOS Settings
| Setting | Value |
| ------ | ------ |
| Fastboot | OFF (Important) |
| CSM | OFF (Important) |
| SecureBoot | OFF |
| IOMMU | OFF |
| AMI Native NVMe Driver | OFF |
| USB Power Delivery in Soft State | OFF |
| fTPM NV for factory reset | OFF |
| Above 4G Decoding | ON |
| Power On By PCIe | ON |
| PCIe16_1 | GEN 3 |

### Tools You Need to Make the Installer:
* ProperTree - used to edit Config.plist
* SSDT-Time - compiled using SSDT-Time (I highly recommend compiling with SSDT-Time instead of using prebuilt ones)
* GenSMBIOS - Used to generate fake SMBIOS for hackintosh
* MountEFI - Necessary if you're making your bootable drive on a Mac or Mac VM
* Gib-MacOS - MacOS downloader script (works on Windows and Linux, but it's recommended to use a Mac for creating the bootable drive)

### Kexts 
* AppleALC - For onboard audio (add alcid=1 to bootargs)
* Lilu - Library for other Kexts
* RealtekRTL8111 - For Ethernet
* VirtualSMC - Essential for system management
* WhateverGreen - For optimizing your graphics card performance 

### SSDTs 
* SSDT-EC - Fake Embedded Controller
* SSDT-USBX - Powers USB devices (e.g., Audio DACs)
* SSDT-SBRG - USB Mapping (If you're using the exact same board, you can copy this SSDT-SBRG and AMDUSBMAP.kext; every port will work just fine.)

If you have a similar system and couldn't get it to boot, feel free to ask for help on my Twitter: [https://twitter.com/Amuu639]

Good luck and have fun hackintoshing.
### Todos
- Benchmarks
