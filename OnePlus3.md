# OnePlus 3 MultiROM Setup Documentation

## A Note About This Document

I have recently sold my OnePLus 3 due to battery bloating issues. It would have cost more to repair than it was worth to me. I never fully succeeded in installing MultiROM (my last attempt to do so resulted in a nearly bricked device that I had to restore using the MSM download tool).

Proceed with caution if you decide to follow the below instructions.

I will no longer be updating this document unless I get a new OnePlus 3.

## Proposed Configuration
- Lineage OS 14.1 (base OS)
- Lineage OS 15 
- CyanogenMod 13
- Oxygen OS
- Kali NetHunter (maybe)
- MIUI 8
- Flyme 6
- Kernel: ElementalX

### A note before proceeding: Make plenty of Nandroid backups, and OFTEN! Any of these steps could be the catalyst for a total reset and you're thrown back to step 1.

## Resetting OnePlus 3 to Stock State
1. Download latest version of Oxygen OS from [OnePlus](http://downloads.oneplus.net/) (when I did this it was 4.5.1)
1. Reboot into recovery by holding power and volume down as the phone boots.
1. Choose the "Install from USB" option in OnePlus Recovery
1. Run the following in terminal on your computer: `adb sideload /path/to/OxygenOS/zip`
1. Allow the phone to reinstall the OS and reboot. Most parts of setup can be skipped since we will be wiping this again soon.

## Installing MultiROM TWRP
1. On the OnePlus 3, reboot into fastboot (I enable advanced reboot in developer settings and use that, but you can use `adb reboot bootloader` if you so choose)
1. Download [MultiROM TWRP](https://forum.xda-developers.com/showpost.php?p=73316166&postcount=1950). When I did this the latest version was 08/07/17.
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

## Installing Lineage OS 14.1
1. Download [Lineage OS 14.1](https://download.lineageos.org/oneplus3). When I did this the latest version was 2017-10-19. Copy to the OP3 using Android File Transfer.
1. Reboot into TWRP recovery using the method of your choice.
1. Wipe the partitions (advanced wipe) and select cache, system, and data.
1. Install the .zip in TWRP. Don't inject MultiROM and do not reboot afterwards.
1. Download [Open GApps](http://opengapps.org/) (I used Stock, the Android version should be 7.1, the Platform should be ARM64) and copy to the device. When I did this the latest version was 2017-10-25.
1. Install GApps in TWRP.
1. Proceed to **Installing Magisk** since we need root access for MultiROM Manager.

## Installing Magisk
1. Download [Magisk](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445). When I did this the latest version was 14.0.
1. Copy this to the device using Android File Transfer.
1. Install this in TWRP but do not inject MultiROM after installation.
1. Proceed to **Installing ElementalX Kernel** since we need a kernel with MultiROM compatibility.

## Installing Custom ElementalX Kernel
1. Download [ElementalX for the OnePlus 3](https://elementalx.org/devices/oneplus-3/). Use the Lineage OS version. The latest version as of this writing is 3.17. 
1. Copy this to the device using Android File Transfer.
1. Install this in TWRP but do not inject MultiROM after installation.
1. Go through the ElementalX installation procedure (I leave my settings stock except for enabling double tap to wake and disabling sweep to sleep).
1. Reboot to system but do not install the TWRP app. We use a custom version of TWRP so it is kind of useless. The standard version of TWRP doesn't have MultiROM capability. If you would like there is an option in TWRP settings to disable prompting to install the TWRP app.

## Installing MultiROM
1. In Security Settings, ensure your device is unencrypted.
1. Download the latest version of [MultiROM for the OnePlus 3](https://forum.xda-developers.com/showpost.php?p=73316166&postcount=1950). When I did this the latest version was 2017-08-07. Copy it to the device and reboot into TWRP.
1. Install the .zip in TWRP. Do not inject MultiROM after installation.
1. Inject the boot sector.
1. Go to MultiROM TWRP Settings and ensure that "Enable no-KEXEC workaround" is checked.
1. Reboot to system.
1. Install the [modded MultiROM Manager](https://androidfilehost.com/?fid=457095661767155476). Check [this post](https://forum.xda-developers.com/showpost.php?p=67685852&postcount=2) to make sure it is the latest version. When I did this the latest version was 2017-04-21.

## Installing LineageOS 15 [WIP]


## Installing CyanogenMod 13 [WIP]
**Last time I tried to do this I bricked my OP3. So a fair note of warning before I attempt this again.**


## Install Oxygen OS [WIP]


## Installing Kali NetHunter [WIP]
**Based on Oxygen OS**

## Installing MIUI 8 [WIP]


## Installing Flyme 6 [WIP]


## Miscellaneous Resources
- [Latest Version of MR TWRP (8/7/17)](https://forum.xda-developers.com/showpost.php?p=73316166&postcount=1950)
- [Decrypting the OP3](https://forum.xda-developers.com/oneplus-3/how-to/unencrypt-oxygenos-loosing-data-t3412228)
- [Default OP3 Encryption Password](https://forum.xda-developers.com/oneplus-3/help/removing-encryption-t3422581) is default_password apparently?
- [Brick Recovery](https://forum.xda-developers.com/oneplus-3/how-to/guide-mega-unbrick-guide-hard-bricked-t3405700)
- [Bricking Info in the MR Thread](https://forum.xda-developers.com/oneplus-3/development/multirom-v33b-op3-t3415654/page100)
