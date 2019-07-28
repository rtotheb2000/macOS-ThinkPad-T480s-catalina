# macOS catalina beta on Lenovo ThinkPad T480s

This repository is a working progress of the clover folder used to install catalina beta on a Lenovo ThinkPad T480s.
I started with https://github.com/linusyang92/macOS-ThinkPad-T480s and realised that an update to catalina beta results in a kernel panic. After some testing I found that the VirtualSMC.kext prevents the installation. So this clover folder excludes this file.

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
- By plugging in an Apple Trackpad 2 via USB I was able to get into the trackpad preference menu (even after unplugging it afterwards). This is only a temporary fix as it is reverted after a restart.

## Issues

- Ethernet (wired)
- Plugging in an external display via USB-C results in reboot (might be fixed, not yet tested ...)
- Sound is not working atm
- Trackpad pref can not be accessed in system Preferences ("Could not load Trackpad preference pane.")
- probably many more that I do not know of yet ...

## List of kexts
| kext  | version | short description |
| ------------- | ------------- | ------------- |
| [AirportBrcmFixup](https://github.com/acidanthera/AirportBrcmFixup) | 1.1.9 | Various patches for Broadcom Airport Wi-Fi cards |
| [AppleALC](https://github.com/acidanthera/AppleALC) | 1.3.9 | Native macOS HD audio for not officially supported codecs |
| [ApplePS2SmartTouchPad](https://github.com/linusyang92/macOS-ThinkPad-T480s) | 4.6.8 | Touchpad support |
| [BrcmBluetoothInjector](https://github.com/RehabMan/OS-X-BrcmPatchRAM) | 2.2.10 | - |
| [BrcmFirmwareData](https://github.com/RehabMan/OS-X-BrcmPatchRAM) | 2.2.10 | - |
| [BrcmPatchRAM2](https://github.com/RehabMan/OS-X-BrcmPatchRAM) | 2.2.10 | - |
| [BT4LEContinuityFixup](https://github.com/acidanthera/BT4LEContinuityFixup) | 1.1.4 | Enable BT4LE-Handoff-Hotspot features |
| [CodecCommander](https://bitbucket.org/RehabMan/os-x-eapd-codec-commander/src/master/) | 2.7.1 | - |
| [HibernationFixup](https://github.com/acidanthera/HibernationFixup) | 1.2.6 | Enable 3 & 25 mode hibernation on certain hardware |
| [Lilu](https://github.com/acidanthera/Lilu/releases) | 1.3.8 | An open source kernel extension bringing a platform for arbitrary kext, library, and program patching throughout the system for macOS |
| [NightShiftUnlocker]( https://github.com/Austere-J/NightShiftUnlocker) | 2.2.1 | Enables Night Shift on all the models |
| [NoTouchID]( https://github.com/al3xtjames/NoTouchID) | 1.0.2 | Disables Touch ID checks causing hangs |
| [RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X) | 2.2.2 | OS X open source driver for the Realtek RTL8111/8168 family |
| [SMCBatteryManager](https://www.hackintosh-forum.de/attachment/105714-e590-zip/) | 1.0 | - |
| [SMCProcessor](https://www.hackintosh-forum.de/attachment/105714-e590-zip/) | 1.0.7 | - |
| [SMCSuperIO](https://www.hackintosh-forum.de/attachment/105714-e590-zip/) | 1.0.4 | - |
| [SystemProfilerMemoryFixup]( https://github.com/Goldfish64/SystemProfilerMemoryFixup) | 1.0.0 | Show memory tab on MacBook models with soldered RAM |
| [USBInjectAll]( https://bitbucket.org/RehabMan/os-x-usb-inject-all/downloads/) | 0.7.1 | - |
| [VirtualSMC]( https://github.com/acidanthera/VirtualSMC/releases) | 1.0.7 | Advanced SMC emulation |
| [WhateverGreen]( https://github.com/acidanthera/WhateverGreen/releases) | 1.3.0 | Various patches necessary for GPUs |

## Related posts
- https://www.hackintosh-forum.de/forum/thread/43618-lenovo-t480s/?postID=518225#post518225
- https://www.tonymacx86.com/threads/t480s-having-problems-updating.280904/page-2
- https://www.hackintosh-forum.de/forum/thread/40836-kurzanleitung-lenovo-thinkpad-t480s/?postID=517939#post517939

## Credits
- https://github.com/linusyang92/macOS-ThinkPad-T480s
- https://www.tonymacx86.com/threads/guide-booting-the-os-x-installer-on-laptops-with-clover.148093
