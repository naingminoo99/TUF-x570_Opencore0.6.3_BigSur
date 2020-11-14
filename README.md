# Tuf x570 Hackintosh Guide
#### BigSur with Everything working ( Apple services,Sleep )
[![N|Solid](https://d2.alternativeto.net/dist/icons/opencore_168788.png?width=64&height=64&mode=crop&upscale=false)](https://github.com/dortania/OpenCore-Install-Guide)

Brief of my Hackintoshing story and Some free tips xD
This guide only focus on Asus Tuf x570 Plus, provided efi might work on similar systems but i don't recommend straight up using it. 
- TIPS
  - Don't use configurators ( most of the tools out there are Clover only supported)
  - Don't follow Youtube Guides (Just read the Dortania Guide it's the only way u can get a stable Hack)
  - Don't Copy other people's EFI (it might boot but u will end up with a problem sooner or later)
  - Doing Your Self is the Fun Part (Knowing what make your hack will help you maintain and troubleshoot alot easier)
  - Read Dortania's Guide for like 2 to 3 times
  - Try again and again and again

### Specifications

- Mobo : Asus TUF X570
- CPU : Ryzen 7 3700X
- GPU : ROG Strix  Radeon RX Vega 64 8GB
- PSU :Superflower 850W 80+ Gold
- RAM : 3200Mhz 32GB (2x16)
- Nvme1 : 500GB
- Nvme2 : 500GB
- Chassis : Corsair iCUE 465x
- AIO : Corsair H100i RGB 
- Fans : Corsair ll120 RGB 
- Network : Fenvi FV-T919

Here is Pc Part Picker Link: [https://pcpartpicker.com/list/43drvf]

### RIG
I name this Ryzenshine since it's all AMD plus it shine so xD
![RyzenshinePic](https://i.imgur.com/Yyophex.jpeg) 

### Bios Setting
| Setting | Value |
| ------ | ------ |
| Fastboot | OFF (Important)|
| CSM |  OFF (Important) |
| SecureBoot |  OFF |
| IOMMU | OFF |
| AMI Native NVme Driver | OFF |
| USB Power Delivery In Soft State | OFF |
| fTPM NV for factory reset | OFF |
| Above 4G Decoding | ON |
| Power On By PCIE | ON |
| PCIE16_1 | GEN 3 |

### Tools You Need to make the installer :
* ProperTree - used to plot Config.plist
* SSDT-Time - compiled using SSDT-Time ( i really recommend compiling with ssdt-time instead of using prebuild one ) 
* GenSMBIOS - Used to generate fake SMBIOS for hack
* MountEFI - U need this if u are making ur bootable on MAC or MACvm
* Gib-MacOS - MacOS Downloader Script ,even tho it work on both windows and Linux I recommend using a mac to make bootable drive.
 (U can only make recovery drives on windows and linux and downloading MacOS through recovery is 
a true pain in the *ss. One second of connection lost and bang u get the Lost connection retry prompt $#%^$%&^)

### KEXTS 
* AppleALC - For on board audio (add alcid=1 to bootargs)
* Lilu - libary for other Kext
* RealtekRTL8111 - for ethernet
* VirtualSMC - the name says it all
* WhateverGreen - to get the most out of ur Graphic card 

### SSDTs 
* SSDT-EC - Fake Embeded Controller
* SSDT-USBX - to power USB devices (eg:Ausio-DACs)
* SSDT-SBRG - USB Mapping 
(if you are using the exatct same board u can copy this SSDT-SBRG and AMDUSBMAP.kext every Port work just fine Thanks me later )

If you have a similar system and couldn't get it to boot feel free to ask for help at my twitter :  [ https://twitter.com/Amuu639 ]


Good Luck and Have Fun Hackintoshing.
### Todos
- Benchmarks

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)
