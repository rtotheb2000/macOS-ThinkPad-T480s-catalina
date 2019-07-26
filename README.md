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

## Working at this point

- Installation of catalina beta using clover v2.4k r4972
- WQHD resolution
- Wireless

## Issues

- Plugging in an external display via USB-C results in reboot
- Sound is not working atm
- Trackpad pref can not be accessed in system Preferences ("Could not load Trackpad preference pane.")
- probably many more that I do not know of yet ...

## Related posts
- https://www.hackintosh-forum.de/forum/thread/43618-lenovo-t480s/?postID=518225#post518225
- https://www.tonymacx86.com/threads/t480s-having-problems-updating.280904/page-2
- https://www.hackintosh-forum.de/forum/thread/40836-kurzanleitung-lenovo-thinkpad-t480s/?postID=517939#post517939

## Credits
- https://github.com/linusyang92/macOS-ThinkPad-T480s
- https://www.tonymacx86.com/threads/guide-booting-the-os-x-installer-on-laptops-with-clover.148093
