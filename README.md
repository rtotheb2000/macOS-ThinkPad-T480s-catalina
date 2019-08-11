# macOS catalina beta on Lenovo ThinkPad T480s

This repository is a working progress of the clover folder used to install catalina beta on a Lenovo ThinkPad T480s.
I started with https://github.com/linusyang92/macOS-ThinkPad-T480s and realised that an update to catalina beta results in a kernel panic. After some testing I found that the VirtualSMC.kext prevents the installation. So this clover folder excludes this file.

I AM RUNNING BETA 5 ATM. BLUETOOTH DOES NOT CONNECT BUT THE ISSUE ALSO APPEARS ON MY MACBOOK AIR SO IT IS NOT SPECIFIC TO HACKINTOSH. IF YOU ARE DEPENDENT ON BLUETOOTH, STAY WITH BETA 4.

## Used Hardware Configuration

- Lenovo ThinkPad T480s (20L8S02D00)
  - Intel i5-8250U
  - 8GB RAM onboard + 8GB Crucial DDR4 2400-SODIMM
  - Samsung 970 evo NVMe 1TB SSD
  - Dell DW1830 Wireless (original Intel AC8265 not working)
  - WQHD display
  - HD Audio Realtek ALC3287

## Working at this point

- WQHD resolution
- WiFi (Dell DW1830)
- Bluetooth (Dell DW1830)
- Ethernet (wired)
- Sound
- Fix for the trackpad pref https://kaykun.net/hf/Trackpad.zip (credit @KayKun from hackintosh-forum.de)
- By plugging in an Apple Trackpad 2 via USB I was able to get into the trackpad preference menu (even after unplugging it afterwards). This is only a temporary fix as it is reverted after a restart.

## Issues

- Plugging in an external display via USB-C (thunderbolt 3) results in reboot
- Trackpad pref can not be accessed in system Preferences ("Could not load Trackpad preference pane.")
- probably many more that I do not know of yet ...

## List of kexts
| kext  | version | short description |
| ------------- | ------------- | ------------- |
| [ACPIBatteryManager](https://github.com/linusyang92/macOS-ThinkPad-T480s) | 1.90.1 | Implements an Advanced Configuration and Power Interface (ACPI) based battery manager kernel extension (kext/driver) for non-Apple laptops running OS X |
| [AirportBrcmFixup](https://github.com/acidanthera/AirportBrcmFixup) | 1.1.9 | Various patches for Broadcom Airport Wi-Fi cards |
| [AppleALC](https://github.com/acidanthera/AppleALC) | 1.4.0 | Native macOS HD audio for not officially supported codecs |
| [ApplePS2SmartTouchPad](https://github.com/linusyang92/macOS-ThinkPad-T480s) | 4.6.8 | Touchpad support |
| [BrcmBluetoothInjector](https://github.com/RehabMan/OS-X-BrcmPatchRAM) | 2.2.10 | - |
| [BrcmFirmwareData](https://github.com/RehabMan/OS-X-BrcmPatchRAM) | 2.2.10 | - |
| [BrcmPatchRAM2](https://github.com/RehabMan/OS-X-BrcmPatchRAM) | 2.2.10 | - |
| [BT4LEContinuityFixup](https://github.com/acidanthera/BT4LEContinuityFixup) | 1.1.4 | Enable BT4LE-Handoff-Hotspot features |
| [CodecCommander](https://bitbucket.org/RehabMan/os-x-eapd-codec-commander/src/master/) | 2.7.1 | - |
| [CPUFriend](https://github.com/acidanthera/CPUFriend) | 1.1.9 | A Lilu plug-in for dynamic power management data injection and prevention of AppleIntelMCEReporter. |
| [CPUFriendDataProvider](https://github.com/acidanthera/CPUFriend) | 1.0.0 | - |
| [HibernationFixup](https://github.com/acidanthera/HibernationFixup) | 1.2.7 | Enable 3 & 25 mode hibernation on certain hardware |
| [IntelMausiEthernet](https://github.com/Mieze/IntelMausiEthernet) | 2.5.0d0 | OS X driver for Intel onboard LAN |
| [Lilu](https://github.com/acidanthera/Lilu/releases) | 1.3.8 | An open source kernel extension bringing a platform for arbitrary kext, library, and program patching throughout the system for macOS |
| [NightShiftUnlocker]( https://github.com/Austere-J/NightShiftUnlocker) | 2.2.1 | Enables Night Shift on all the models |
| [NoTouchID]( https://github.com/al3xtjames/NoTouchID) | 1.0.2 | Disables Touch ID checks causing hangs |
| [NullEthernet](https://github.com/RehabMan/OS-X-Null-Ethernet) | 1.0.6 | Enables Mac App Store access even if you don’t have a built-in Ethernet port with supporting drivers |
| [RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X) | 2.2.2 | OS X open source driver for the Realtek RTL8111/8168 family |
| [USBPorts]( https://github.com/linusyang92/macOS-ThinkPad-T480s) | 1.90.1 | - |
| [VirtualSMC]( https://github.com/acidanthera/VirtualSMC/releases) | 1.0.7 | Advanced SMC emulation |
| [WhateverGreen]( https://github.com/acidanthera/WhateverGreen/releases) | 1.3.1 | Various patches necessary for GPUs |

## Related posts
- https://www.tonymacx86.com/threads/lenovo-t480s-a-noobs-approach.281330/
- https://www.hackintosh-forum.de/forum/thread/43618-lenovo-t480s/?postID=518225#post518225
- https://www.tonymacx86.com/threads/t480s-having-problems-updating.280904/page-2
- https://www.hackintosh-forum.de/forum/thread/40836-kurzanleitung-lenovo-thinkpad-t480s/?postID=517939#post517939

## Credits
- https://github.com/linusyang92/macOS-ThinkPad-T480s
- https://www.tonymacx86.com/threads/guide-booting-the-os-x-installer-on-laptops-with-clover.148093
