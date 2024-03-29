# Asus-X540LJ-Hackintosh-macOS-Sonoma-OpenCore

# Asus Vivobook X540LJ
- **Bootloader:** OpenCore 0.9.7
- **macOS:** 14.2.1 Sonoma

# Changelog
### Update: 05-Jan-2024
- Initial Release of macOS Sonoma

<img src="DOC/macOS Sonoma Asus x540LJ.jpg" width="900px" alt="Asus X540LJ macOS Sonoma OpenCore Hackintosh">

# Specification:
- **MainBoard:** Asus X540LJ.
- **Processor:** Intel Core i3-5005U @ 2.0GHz (Broadwell)
- **RAM:** 8GB DDR3 1600mhz (Duel channel)
- **Graphic:** 
  + Intel HD5500
  + NVIDIA GeForce 920M 2GB
- **Network:**
  + **Wifi:** Atheros AR9565
  + **Ethernet:** Realtek RTL810xE
- **Audio:** Realtek ALC255
- **Touchpad:** ELAN 1100 (I2C)
- **SD Card Reader** Realtek RTS5286
- **Storage**: 240GB SSD, 1TB HDD

# WORKING:
- [x] Power Management
- [x] Intel HD Graphics 5500 (OCLP patch needed)
- [x] Sound **(Internal Speaker and Headphone working)**
- [x] Mic **(Internal and External both working)**
- [x] SD Card Reader
- [x] Ethernet
- [x] Adjust brightness 
- [x] USB 2.0, 3.0, Type-C
- [x] Trackpad **(All gestures supported)**
- [x] Sleep  **(working while using battery. Will not work in power connected mode)**
- [x] Battery Stat 
- [x] Tempareture Monitor 
- [x] Apple Store, iCloud, FaceTime, iMessege
- [x] Fn feature **(Brightness and volume button works)**

# Not WORKING:
- [ ] Nvidia 920M GPU   **(will never work)**
- [ ] Wifi (USB Wifi adapter needed)
- [ ] Bluetooth (USB BT adapter needed)

# Installation:

### Download this before Install:
- `OCLP(OpenCore Legacy Patcher)`  `EFI Mounter`  `Provided EFI with Config folder` & most important `Patience`

### BIOS Settings
- No need to change any BIOS settings. Set default BIOS settings.
- If you use extra monitor then disable `Launch CSM` in BIOS boot section.

### Installing macOS Sonoma:
- Change the default BIOS settings.
- Just put this EFI to your USB EFI partition.
- If you don't know how to make bootable your USB then go [here.](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
- Install macOS Sonoma to your SSD or HDD.
- If you are new then go [here.](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html#prerequisites)
- After install mount the USB EFI and copy this to your HDD or SSD EFI.
  
### Fixing Graphics Driver:
- Copy the 2nd config file `Configs > config 2 > config.plist` then past/replace it to your SSD EFI folder that located `EFI > OC`
- Reboot your laptop.
- Open OCLP (OpenCore Legacy Patcher) & install root patch `OCLP > Post Install Root Patch > Start Root Patching`
- After fininishing the patching Reboot your laptop.

### iMessege & Facetime Fix:
- Change the serial numbers and other things. You can find the tutorial from [here.](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/broadwell.html#platforminfo)

### SSD Fix:
- If you use SSD then you have to enable TRIM Support for better performance.
- Go to the Terminal and type `sudo trimforce enable`
- Then type **Y** and enter.
- Again type **Y** and enter.

### Wifi & Bluetooth:
- My Wifi & Bluetooth are from Atheros. It doesn't work on it. So that I use USB wifi adapter. If your wifi is not from Atheros then find the solution from google.

### Updating macOS:
- I will give you the detail guide later.

## Credits
@RehabMan for his guide for beginner
@alexandred and his team for VoodooI2C 
@acidanthera for his OpenCore Bootloader and kexts
and many more people that I can't list here.
