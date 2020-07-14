# OnePlus One (bacon) ROM Documentation

1. Reboot to fastboot with `adb reboot bootloader`
2. Unlock bootloader (will wipe data): `fastboot oem unlock`
3. Install [TWRP Recovery](https://twrp.me/oneplus/oneplusone.html) with the command `fastboot flash recovery twrp.img` where `twrp.img` is the filename of the TWRP recovery file.
4. Reboot into recovery.
5. Install the latest version of [LineageOS](https://download.lineageos.org/bacon) and the associated [GApps](https://opengapps.org/) (ARM, Android 9.0). Lineage must be flashed first, then GApps.
6. (optional, before rebooting) Install [Magisk](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445) for root.
7. Reboot into your new system.
