# Nexus 5 MultiROM Setup Documentation

## Resetting Nexus to Stock State
1. Download Nexus Factory Stock Image (https://developers.google.com/android/images#hammerhead)
2. Reboot Nexus to fastboot with: `adb reboot booloader`
3. Unlock bootloader: `fastboot oem unlock`
4. Flash stock image to Nexus (`cd` into the directory where the stock image was unzipped to first): `./flash-all.sh`
5. Reboot into the new stock image
6. Set up stock image (you can skip most of the configuration since we'll be wiping it soon)
7. Enable developer options in stock image
8. Enable USB debugging in developer settings and authorize your computer
9. Reboot Nexus to fastboot with: `adb reboot booloader`

## Installing LineageOS 14.1, MultiROM, MultiROM TWRP, and ElementalX
10. Download modded MultiROM TWRP and modded MultiROM (https://basketbuild.com/devs/Captain_Throwback/Nexus%205/MultiROM)
11. Install modded TWRP recovery with: `fastboot flash recovery /path/to/twrp/file`
12. Use volume buttons to reboot to recovery
13. Swipe to allow modifications.
14. Download Open GApps for Android versions: 4.4, 5.1, 6.0, 7.1 (I like the Pico versions best) (http://opengapps.org)
15. Download ElementalX Kernel for Nexus 5 (http://elementalx.org/devices/nexus-5/)
16. Using TWRP, wipe the stock ROM (Wipe all the partitions)
17. Copy OpenGApps, ElementalX, modded MultiROM, and LineageOS 14.1 to the Nexus using Android File Transfer
18. Install LineageOS 14.1 using TWRP (Don't inject MultiROM yet)
19. Install OpenGApps for Android 7.1 (Don't inject MultiROM yet)
20. Reboot into LineageOS and go through setup
21. Enable developer options in LineageOS and authorize your computer
22. Reboot back into TWRP
23. Swipe to allow modification (check never show again if you don't want to be asked again)
24. Install ElementalX (Don't inject MultiROM yet)
25. Reboot system to ensure ElementalX installation worked
26. Reboot back into TWRP
27. Install modded MultiROM
28. Inject current boot sector
29. Reboot to test if MultiROM installation worked (you should see the MultiROM menu)

## Installing Plasma Mobile - Internal Storage
30. Reboot back into TWRP
31. Tap 3 bars in corner, then Add ROM, then choose the CM-Stripped ROM and install it
32. Reboot into the CM-Stripped ROM and give it about 5 minutes to let it boot (It will be at the Google logo)
33. On your computer, restart adb as root: `adb root`
34. Run the Plasma Mobile flashing script on your computer (make sure the Nexus is connected of course) (if needed `chmod +x` the script)
35. Once the script is finished, the Nexus will reboot and if you don't catch it in time it will boot to Lineage. If it does just reboot back into cm-stripped
36. Test out Plasma Mobile, make sure it boots (Plasma Mobile is still in a developmental stage so a lot of stuff is broken right now)

## Installing SuperSU
37. Reboot back to TWRP
38. Flash SuperSU (https://download.chainfire.eu/1021/SuperSU/SR3-SuperSU-v2.79-SR3-20170114223742.zip)
39. Reboot back to LineageOS

## Installing Ubuntu Touch - Internal Storage
40. Install the modded .apk of MultiROM Manager (the Ubports version)
41. Reboot back to TWRP
42. Install standard MultiROM (https://forum.xda-developers.com/google-nexus-5/orig-development/mod-multirom-v24-t2571011)
43. Reboot back to LineageOS
44. From MultiROM Manager, install Ubuntu Touch (stable version 13 is what I use). Reboot into recovery when asked.
45. Boot Ubuntu Touch to make sure the install worked

## Installing Sailfish OS - Internal Storage
46. Reboot to fastboot
47. Download MultiROM TWRP (https://forum.xda-developers.com/google-nexus-5/orig-development/mod-multirom-v24-t2571011)
48. Flash MultiROM TWRP to Nexus: `fastboot flash recovery /path/to/twrp`
49. Boot into TWRP and add a ROM of type Sailfish OS
50. Select the CM11 Snapshot M11 zip as the CyanogenMod zip and the Sailfish zip as the rootfs zip
51. Boot SailfishOS to make sure it works

## Installing Patched MultiROM, MultiROM TWRP, and MultiROM Manager For Optimal Compatibility
52. Reboot into fastboot bootloader
53. Flash Updated TWRP For Nougat ROM Compatibility (https://www.androidfilehost.com/?w=files&flid=102780)
54. Reboot back into LineageOS and uninstall the both the Google Play version and the old Ubports version of MultiROM Manager. Install the new Ubports version located here: (https://forum.xda-developers.com/showpost.php?p=71471699&postcount=3668). 

## Installing CyanogenMod 11 - USB Storage
55. Reboot back into TWRP and mount USB OTG
56. Add a new ROM in MultiROM Settings
57. Select the CyanogenMod 11 .zip
58. Set the image sizes: 436MB for cache, 4095MB for data, 1024MB for system
59. Swipe to confirm and install the ROM.
60. Once the ROM is flashed, go back "home" in TWRP and return to the MultiROM section.
61. List the ROMs and select USB OTG as your storage. Select the CM11 ROM. 
62. Tap "Install zip" and install the Open GApps 4.4 zip. (If you get errors about ot being able to mount the disk just reboot out of and back into TWRP)
63. Go back into MultiROM settings in TWRP and inject the boot sector.
64. Reboot and select the CM11 ROM (It will be under the external storage tab). Set up the CM 11 ROM as necessary.

## Installing CyanogenMod 12 - USB Storage
65. Reboot back into TWRP and get into the MultiROM section
66. Add the CyanogenMod 12 ROM, installing to USB, using the same image sizes as CM11: 436MB for cache, 4095MB for data, 1024MB for system
67. Flash the GApps 5.1 zip onto CM12 (see steps 60-63 for instructions, just adjust for CM12).
68. Go back to MultiROM settings in TWRP, and inject the boot sector. 
69. Reboot the system into CyanogenMod 12 to test it out. Set it up as necessary.

## Installing CyanogenMod 13 - USB Storage
70. Reboot back into TWRP and get into the MultiROM section
71. Add the CyanogenMod 13 ROM, installing to USB, using the same image sizes as CM11/12: 436MB for cache, 4095MB for data, 1024MB for system (these are the same image sizes as CM11 and CM12)
72. Flash the GApps 6.0 zip onto CM13 (see steps 60-63 for instructions, just adjust for CM13).
73. Go back to MultiROM settings in TWRP, and inject the boot sector. 
74. Reboot the system into CyanogenMod 13 to test it out. Set it up as necessary.

## Installing Firefox OS - USB Storage
75. Reboot back into TWRP and get into the MultiROM section
76. Add the Firefox OS 2.6 ROM (https://ffos.vosky.fr), installing to USB and with image sizes: 436MB for cache, 4095MB for data, 1024MB for system.
77. Go back to MultiROM settings in TWRP, and inject the boot sector.
78. Reboot the system into Firefox OS to test it out. Set it up as necessary.

## Uninstalling SuperSU and Installing Magisk
79. Reboot into Lineage OS and open the SuperSU app.
80. Go into SuperSU Settings and uncheck "Enable Superuser".
81. Reboot back into Lineage OS and return to SuperSU Settings
82. Select the "Full Unroot" option, *do* restore the stock boot image but *do not* restore stock recovery.
83. Download Magisk (https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)
84. Reboot into TWRP and flash the Magisk zip.
85. Inject the current boot sector.
86. Reboot into LineageOS and uninstall the Magisk Manager
87. Update to the new Magisk Manager from the Play Store.

## Installing NexSense (HTC Sense Port) - USB Storage
88. Download NexSense ROM zip (https://forum.xda-developers.com/google-nexus-5/development/port-nexsense-sense-6-0-wifi-fix-m8-t2703397) and NexSense ROM Patches zip (same link).
89. Add an Android ROM and choose NexSense_ALPHA-GalaxyUser.zip, using the USB storage.
90. Use the same image sizes as CM11/12: 436MB for cache, 4095MB for data, 1024MB for system
89. Navigate to the new ROM's settings and flash the NexSense_Path-GalaxyUser.zip file.
90. Boot into Sense and set it up as necessary.

## Installing MIUI 8 - USB Storage
91. Download MIUI 8 ROM (https://forum.xda-developers.com/google-nexus-5/development/rom-miui-8-6-3-30-t3409440).
92. Reboot into TWRP and add a new Android ROM, installing to USB. Use the image sizes: 436MB for cache, 4095MB for data, 2048MB for system.
93. Go back to MultiROM settings in TWRP, and inject the boot sector. 
94. Boot into MIUI and set it up as necessary.

## Installing Kali NetHunter - Internal Storage
91. Download Kali NetHunter (https://www.offensive-security.com/kali-linux-nethunter-download/).
92. Add a new CyanogenMod 13 ROM installed to internal storage
93. Flash OpenGApps 6.0 to this ROM
94. Flash SuperSU (https://download.chainfire.eu/1021/SuperSU/SR3-SuperSU-v2.79-SR3-20170114223742.zip) to this ROM.
95. Boot into the new ROM to set it up to a base state (there will not be any Kali stuff on it yet).
96. Reboot back into TWRP and flash the NetHunter zip onto the new ROM.
97. The installation may graphically freeze at any point and it will look as if no progress is being made. Make sure that there is no graphical movement on screen (the Aroma progress bar for the installer will normally show some slight activity and pulse with light) and that at least 10-20 minutes have elapsed since the freeze, and force reboot.
98. Boot into NetHunter and set it up as necessary.