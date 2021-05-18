# ThinkPad T470 OpenCore 

![alt text](https://github.com/asrjy/T470-Hackintosh/blob/main/Screenshots/about.png?raw=true)
![alt text](https://github.com/asrjy/T470-Hackintosh/blob/main/Screenshots/neofetch.png?raw=true)

This is my first attempt at a (almost) fully functional Hackintosh for ThinkPad T470. Got it to work after lots of errors and research. I recommend you to go through [Dortonia's Guide](https://dortania.github.io/OpenCore-Install-Guide/) even if you are going to use my EFI. 

### Specs
| Component | Name |
| ------ | ------ |
| CPU   | i5-6300U |
| Graphics | HD 520 |
| RAM | 8 GB |
| Display | 14.0" (355mm) HD 1366x768 |
| Storage | SanDisk SSD Plus 256 GB  |
| Network | Intel Dual Band Wireless-AC 8260 |
| Network | Intel Dual Band Wireless-AC 8260 |

### Kexts Used:
- AirportItlwm
- AppleALC
- BrightnessKeys
- CpuTscSync
- ECEnabler
- IntelMausi
- Lilu
- NVMeFix
- SMCBatteryManager
- SMCLightSensor
- SMCProcessor
- SMCSuperIO
- USBInjectAll
- VirtualSMC
- VoodooPS2Controller(RehabMan's Version)
- WhateverGreen

### What's Working?
Almost everything except
- Wi-FI. There's a kext called AppleIntelWifi that's supposed to work but it did not work for me. 
- The Power Indicator blinks even after waking up from Sleep. 
- Magic Gestures do not work. However acidanthera's VoodooPS2Controller had Magic Gestures, but no Tap to Click. 
- TrackPoint is a bit laggy. Usable, slight inconvenience.

#### Audio Codec: ALC 298, layout 47 in the boot-args worked for me. Try various options.

### Installation
- The best way to get the ACPI files is to boot into a live linux disk and use SMDTTime to generate the DSDT dump and the .aml files. Using pre built files may prolong the boot time. 
- Following the Documentation carefully will guarentee the best possible 
- Generate the SMBIOS using GenSMBIOS to be able to use Apple Software. 
