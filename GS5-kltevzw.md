# Verizon Galaxy S5 (kltevzw)
Note: While this is designed for the Verizon varient, many parts can also be used on the global varient (klte). The steps that can only be used on kltevzw will be marked as such.

## Root (kltevzw)
Root can be achieved via different methods depending on what build you are on.

| Android base | Build | Method                                  |
|:------------ |:----- |:---------------------------------------:|
| KitKat       | `NCG` | [TowelRoot](#towelroot)                 |
| KitKat       | `NE9` | [KitKat Root](#kitkat-root-kltevzw)     |
| KitKat       | `NHA` | [KitKat Root](#kitkat-root-kltevzw)     |
| KitKat       | `NI2` | [KitKat Root](#kitkat-root-kltevzw)     |
| KitKat       | `NK2` | [KitKat Root](#kitkat-root-kltevzw)     |
| Lollipop     | `OA8` | Not Possible!                           |
| Lollipop     | `OC2` | Not Possible!                           |
| Lollipop     | `OD5` | Not Possible!                           |
| Lollipop     | `OE1` | [Lollipop Root](#lollipop-root-kltevzw) |
| Lollipop     | `OK3` | [Lollipop Root](#lollipop-root-kltevzw) |
| Lollipop     | `OG5` | [Lollipop Root](#lollipop-root-kltevzw) |
| Lollipop     | `PB1` | [Lollipop Root](#lollipop-root-kltevzw) |
| Marshmallow  | `PF4` |        |
| Marshmallow  | `PG2` |        |
| Marshmallow  | `PJ2` |        |
| Marshmallow  | `PF4` |        |
| Marshmallow  | `PL1` |        |
| Marshmallow  | `QA1` |        |
| Marshmallow  | `PL1` |        |
| Marshmallow  | `QB2` |        |
| Marshmallow  | `PL1` |        |
| Marshmallow  | `QC2` |        |
| Marshmallow  | `PL1` |        |
| Marshmallow  | `QD1` |        |
| Marshmallow  | `PL1` |        |

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

