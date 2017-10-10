# OnePlus 3 MultiROM Setup Documentation

## Proposed Configuration
- Oxygen OS (base OS)
- LineageOS 15 
- LineageOS 14.1
- CyanogenMod 13
- Kali NetHunter (maybe)
- MIUI 8
- Flyme 6


## Resetting OnePlus 3 to Stock State
1. Download latest version of Oxygen OS from [OnePlus](http://downloads.oneplus.net/) (as of this writing it's 4.1.7)
1. Reboot into recovery by holding power and volume down as the phone boots.
1. Choose the "Install from USB" option in OnePlus Recovery
1. Run the following in terminal on your computer: `adb sideload /path/to/OxygenOS/zip`
1. Allow the phone to reinstall the OS and reboot. Most parts of setup can be skipped since we will be wiping this again soon.

## Installing MultiROM TWRP
1. On the OnePlus 3, reboot into fastboot (I enable advanced reboot in developer settings and use that, but you can use `adb reboot bootloader` if you so choose)
1. Download MultiROM TWRP: [Latest version as of 10/9/17 - Version 08/07/17](https://forum.xda-developers.com/showpost.php?p=73316166&postcount=1950)
1. On your computer with the OP3 plugged in run the command: `fastboot oem unlock`. **WARNING THIS WILL WIPE ALL DATA ON THE DEVICE.** Use the volume buttons to select yes and then the power button to confirm.
1. Once the phone displays the boot selection menu press the volume keys to cancel automatic boot and access the Boot Options Menu. Boot into Fastboot again.
1. On your computer: `fastboot flash recovery /path/to/twrp/img`
1. On your computer: `fastboot reboot`. Then press the volume keys to cancel automatic boot again, and this time choose Recovery. The boot options menu will show again, DO NOT make a change and let it boot into TWRP.
1. When prompted for a password press cancel.
1. Swipe to allow modifications
1. When in TWRP, choose "Reboot" then "Bootloader" to return to Fastboot.
1. On your computer, with the OP3 plugged in: `fastboot format userdata`
1. Use the volume buttons on the OP3 to reboot back into TWRP
1. Swipe to allow modifications. Now you are in TWRP.

## Installing Custom ElementalX Kernel
1. Download [ElementalX for the OnePlus 3](https://elementalx.org/devices/oneplus-3/)
1. Copy this to the device using Android File Transfer.
1. Install this in TWRP but do not inject MultiROM after installation.
1. Go through the ElementalX installation procedure (I leave my settings stock except for enabling double tap to wake and disabling sweep to sleep)
1. Reboot to system but do not install the TWRP app. We use a custom version of TWRP so it is kind of useless. The standard version of TWRP doesn't have MultiROM capability

## Installing MultiROM [WIP]


## Installing LineageOS 15 [WIP]


## Installing LineageOS 14.1 [WIP]


## Installing CyanogenMod 13 [WIP]


## Installing Kali NetHunter [WIP]


## Installing MIUI 8 [WIP]


## Installing Flyme 6 [WIP]


## Resources
[Latest Version of MR TWRP (8/7/17)](https://forum.xda-developers.com/showpost.php?p=73316166&postcount=1950)
