# HP Z440 OpenCore

![alt text](https://i.imgur.com/lYTBVfX.png)

## Overview
This is the Hackintosh Opencore EFI for the HP Z440 Workstation. Available for most HP Z440 Workstation Models. 
## Specs

<p><i>This is the specs of my specific HP Z440. Should be similar to yours.</i></p>

| Part             | Description                                                                                                    |
| ---------------- | -------------------------------------------------------------------------------------------------------------- |
| CPU              | Intel® Xeon® Processor E5-1650 v3                                                                              |
| GPU              | AMD Radeon™ R9 390X                                                                                            |
| Memory           | 64Gb (4 x Samsung 8Gb 2133MHz)                                                                                 |
| Storage          | Sillicon Power A55 512GB 2.5" SATAIII 6 Gbps SSD                                                               |
| Display          | Dell S2421H 24 Inch (HDMI) 1920x1080                                                                           |
| Wifi & Bluetooth | Apple Airport Broadcom BCM4360  (Fenvi T919)                                                                   |
| LAN              | Intel® Gigabit Ethernet, 10/100/1000                                                                           |                             
| Audio            | Realtek ALC221 (alcid=11)                                                                                      |
| External ports   | 4 x USB 3.0 Front, 4 x USB 3.0 Back, 2 x USB 2.0 Back (NOT WORKING)                                            |

<h2>What works and what doesn't work?</h2>

| Part                                                             | Status | Note                           |
| ---------------------------------------------------------------- | ------ | -----------                    |
| RJ45 LAN Port                                                    | ✅     |                                 |
| Audio.                                                           | ✅     |  With several patches. No front panel audio.          |
| Wifi                                                             | ✅     |  With Fenvi T919               |
| Bluetooth                                                        | ✅     |  With Fenvi T919               |
| USB                                                              | ✅     |  Except Back USB 2.0           |
| Sleep                                                            | ✅     |                                |
| Handoff                                                          | ✅     |                                |
| Airdrop                                                          | ✅     |                                |
| AMD dGPU                                                         | ✅     |                                |
| DRM                                                              | ✅     |  iMac Pro SMBIOS               |


## How to use?

### Download EFI

- <a href="https://github.com/ahnaf2012/HP-Z440-OpenCore/releases/">
    <img src="https://img.shields.io/github/v/release/ahnaf2012/HP-Z440-Opencore?label=macOS%20Monterey&color=bright-green" />
  </a>


### Edit the efi you just downloaded

<p align="center">
  <img src="https://dortania.github.io/OpenCore-Install-Guide/assets/img/smbios.46661610.png" style="margin: auto;"/>
</p>

- Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate SMBIOS.
- Use [ProperTree](https://github.com/corpnewt/ProperTree) to add SMBIOS information to config.plist file.
- Use iMacPro1,1 for SMBIOS. 

### Create boot

- Format your USB to `fat32`.
- Copy folder `EFI` to your USB.
- Create folder `com.apple.recovery.boot` in your USB.
- Download `macOS Recovery` - follow [here](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
- Copy 2 files `BaseSystem.dmg` & `BaseSystem.chunklist` to folder `com.apple.recovery.boot`.

### Installing

- Follow [here](https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html)

### Credits

[@misa198](https://github.com/misa198) - For README template inspiration.

[@acidanthera](https://github.com/acidanthera) and [@corpnewt](https://github.com/corpnewt) and rest - For making this possible

[@apple](https://www.apple.com/macos) - For making macOS
