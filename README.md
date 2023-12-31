# Rayzen-iGPU-B450-hackintosh
OpenCore EFI for B450 Chipset Motherboard with AMD Ryzen 6 cores with iGPU

WARNING ⚠️: I  do not responsible for lost personal data, or malfunction hard drive. **You are doing this at your own RISK.**
|  Components             |         Requirements                |            Note                      |
|-------------------------|-------------------------------------|--------------------------------------|
| CPU                     |  6 cores AMD CPU                  |  This EFI is using a 6 cores kernel patch. If your CPU have more or less cores than this EFI, change it and refer to the OpenCore guide. |
| GPU                     |  AMD Vegas iGPU        | Thanks to NootedRed to get AMD iGPU support on this Hackintosh! Make sure that you don't have a dGPU in your system! |
| Motherboard             | B450 motherboards            |  This build will only work for the B450 motherboards, for other, please refer to the OpenCore Guide.|
| RAM                     | 2 x 16GB + 8GB DDR4 3200Mhz  |  |
| Ethernet  | Realtek RTL8111 Gigabit Ethernet |  |
| Audio     | Realtek ALC892 | |
| OS | macOS Ventura 13.5 | |

## Settings to change

|BIOS Settings|Toggle|
|-------------------------|-------------------------------------|
|Secure Boot|**OFF**|
|TPM|**OFF** (optional)|
|Above 4G Decoding|**ON**|
|VRAM for iGPU|Above 512M for best results|
|Fast Boot|**OFF**|
|CSM|**OFF**|
|Serial Port|**OFF**|

## Whats Work?

- CPU Power Management
- Shutdown , Restart and Sleep
- Ethernet
- Bluetooth
- HDMI
- Audio (Rear & Front)
- TRIM Support for SSD
- Etc

## Tutorial
- From Zero Tutorial : https://dortania.github.io/OpenCore-Install-Guide/
- Creating the USB Installer : https://dortania.github.io/OpenCore-Install-Guide/installer-guide/
- Generating SMBIOS : https://github.com/corpnewt/GenSMBIOS
- USB Fixes : https://dortania.github.io/OpenCore-Post-Install/usb/ and https://github.com/usbtoolbox/tool

Tutorial on "USB Fixes" related to the UTBMap.kext and SSDT-SLEEP.aml files. Please pay close attention to the guidelines that have been provided.

## Remark
- i have Asus TUF gaming B450 pro II , so please note that some usb ports won't work for u, if they didn't delete the USBMap.kext and use a compatible one for ure MB by using USBToolBox.
- when the bootloader crash while the instalation please remove the nootedred.kext and save it anywhere and reolace it with whatevergreen.kext, when the instalation is done return everything to its place.(the nootedred.kext is used for making the igpu compatible whith macos sys)
