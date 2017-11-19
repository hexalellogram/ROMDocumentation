# Verizon Galaxy S5 (kltevzw)
Note: While this is designed for the Verizon varient, many parts can also be used on the global varient (klte). The steps that can only be used on kltevzw will be marked as such.

- [Root (kltevzw)](#root-kltevzw)
- [Bootloader unlock (kltevzw)](#bootloader-unlock-kltevzw)
- [Custom Recovery](#custom-recovery)
- [ROMs](#roms)

## Root (kltevzw)
Root can be achieved via different methods depending on what build you are on.

The required information: "Android base" and "build" can be located in the device settings. 

Go to "Settings -> About Phone" and check "Android Version"

If you have `4.4.x` you have `KitKat`

If you have `5.x.x` you have `Lollipop`

If you have `6.x.x` you have `Marshmallow`

This will give you the "Android Base" information.

To get the "Build" information, go to "Settings -> About Phone" and check "Build". Get the last 3 characters of this long string. 

Use that information to follow the table and identify the proper rooting method

| Android base | Build | Method                                        |
|:------------ |:----- |:---------------------------------------------:|
| KitKat       | `NCG` | [TowelRoot](#towelroot)                       |
| KitKat       | `NE9` | [KitKat Root](#kitkat-root-kltevzw)           |
| KitKat       | `NHA` | [KitKat Root](#kitkat-root-kltevzw)           |
| KitKat       | `NI2` | [KitKat Root](#kitkat-root-kltevzw)           |
| KitKat       | `NK2` | [KitKat Root](#kitkat-root-kltevzw)           |
| Lollipop     | `OA8` | Not Possible!                                 |
| Lollipop     | `OC2` | Not Possible!                                 |
| Lollipop     | `OD5` | Not Possible!                                 |
| Lollipop     | `OE1` | [Lollipop Root](#lollipop-root-kltevzw)       |
| Lollipop     | `OK3` | [Lollipop Root](#lollipop-root-kltevzw)       |
| Lollipop     | `OG5` | [Lollipop Root](#lollipop-root-kltevzw)       |
| Lollipop     | `PB1` | [Lollipop Root](#lollipop-root-kltevzw)       |
| Marshmallow  | `PD1` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `PF4` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `PG2` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `PJ2` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `PF4` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `PL1` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `QA1` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `PL1` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `QB2` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `PL1` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `QC2` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `PL1` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `QD1` | [Marshmallow Root](#marshmallow-root-kltevzw) |
| Marshmallow  | `PL1` | [Marshmallow Root](#marshmallow-root-kltevzw) |

### TowelRoot
kltevzw: Only works on `NCG`
klte: Should work on many/all KitKat builds
1. Visit the [TowelRoot](https://towelroot.com/) site
1. Tap on the lambda to download the APK
1. Install the APK and run.
1. Ignore any security issues it shows
1. Tap `Make it Ra1n!`
1. Reboot

### KitKat Root (kltevzw)
Follow these steps for all KitKat builds other than `NCG`

1. Note your build
1. Download the `NCG` kernel
1. Flash the downloaded `NCG` kernel with Odin
1. Reboot
1. Use TR to root
1. Download the kernel for the build you originally were on (Noted from step 1)
1. Flash the downloaded kernel with Odin
1. Reboot

### Lollipop Root (kltevzw)
Note that this is not recommended! The preferred way is to use the [Marshmallow root] method, but this will work for the noted builds

1. Note the build for your ROM
1. Download [this file](https://androidfilehost.com/?fid=24438995911970571) and unzip
1. Open Odin, and reboot your phone in download mode
1. Flash `G900VVRU2BPB1_G900VVZW2BPB1_G900VVRU2BPB1_HOME.tar.md5` that was in the folder downloaded in step 1
1. Reboot your phone, and skip setup (don't add any accounts).
1. Download [this root file](https://androidfilehost.com/?fid=312968873555011514) and unzip
1. Run `1 - Install APK's.bat` or install `KROOT.apk`, `busybox.apk`, and `Safestrap.apk` from the folder
1. Run `2 - Flash NK2.bat` or reboot to download mode
1. Flash `NK2_Kernel.tar` with Odin
1. Run `3 - Root Process.bat`
1. If it succeeds, continue, otherwise pull the battery, remove the USB cable, reinsert the battery, hold the power button until the phone vibrates, then re-run `3 - Root Process.bat`
1. Run `4 - Flash PB1.bat` or reboot to download mode
1. Flash the kernel with the build for your ROM, as noted in step 1.

### Marshmallow Root (kltevzw)
This is the recommended root method. 

1. Download [This app](https://androidfilehost.com/?fid=673368273298935345) and install
1. Note the first 2 numbers in the eMMC box, under CID

| eMMC CID | Root Method                                                                |
|:-------- |:--------------------------------------------------------------------------:|
| 15       | [Root and bootloader unlock](#marshmallow-emmc-15-root-bootloader-kltevzw) |
| 11       | [Root only](#marshmallow-emmc-11-root-kltevzw)                             |
| Other    | Not possible!                                                              |

### Marshmallow eMMC 15 Root Bootloader (kltevzw)

### Marshmallow eMMC 11 Root (kltevzw)


## Bootloader unlock (kltevzw)

The bootloader can be unlocked if you have a Samsung eMMC. Some phones have a Toshiba eMMC and some have a Samsung eMMC. There are two ways to identify which eMMC your phone has.

Option 1:
1. Download [This app](https://androidfilehost.com/?fid=673368273298935345) and install
1. Note the first 2 numbers in the eMMC box, under CID

Option 2:
1. Open this file using ADB or a file explorer: `/sys/block/mmcblk0/device/cid`
1. Read the first 2 numbers

If you have the first 2 numbers with "11", you can't unlock the bootloader.

If you have the first 2 numbers with "15", wonderful! We can continue with the unlock process.

In order to unlock the bootloader, your phone MUST be rooted! If you are already on Marshmallow, go back to the root section and root your phone. This will automatically unlock your bootloader. If you are not on Marshmallow, you can either update to Marshmallow (OTA) or root your phone using the previous methods. The easiest is to take the Marshmallow OTA since rooting Marshmallow and unlocking the bootloader simeltaneiously is easier than the other methods.

NOTE: IF YOU ARE ROOTED ON LOLLIPOP ON ONE OF THE FOLLOWING BUILDS, YOU ARE IN LUCK!!!
- `OE1`
- `OK3`
- `PB1`

1. Download [this](https://androidfilehost.com/?fid=24459283995314681)
1. Install flashfire or safestrap
1. Flash the downloaded file using safestrap or flashfire
1. Run the "SamsungUnlocker" app
1. Grant SuperSU access
1. Type "yes" in the terminal when the prompt appears
1. After the phone turns off, boot the device to bootloader and verify that the status shows as "Developer"
1. Flash TWRP using Odin

## Custom Recovery
If the bootloader has been unlocked on a kltevzw, or you are using a klte, TWRP can be installed using Odin.

Follow the steps on the [TWRP documentation](https://twrp.me/samsung/samsunggalaxys5qualcomm.html) to install it

## ROMs
ROMs can be installed on this phone just like any other Android phone, granted the bootloader has been unlocked

If you have a kltevzw with a Toshiba eMMC (11), only ROMs that specify a bootloader unlock is not required will work.

If you have a kltevzw with an unlocked bootloader (Samsung eMMC (15) or developer edition), most Galaxy s5 ROMs can be installed.
Note that some ROMs have a seperate version for the kltevzw. Be sure to check if the unified klte build will work on the kltevzw. One notable example is LineageOS. The builds were seperate until March 2017 when they were unified.

Regardless, be sure the ROM is for the "klte", the "Qualcomm Galaxy s5", the "GT-900F", etc. Make sure it does NOT say "LTE+" or "Exynos"
