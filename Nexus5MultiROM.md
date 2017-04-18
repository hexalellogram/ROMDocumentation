# Nexus 5 MultiROM Setup Documentation

1. Download Nexus Factory Stock Image (https://developers.google.com/android/images#hammerhead)
2. Reboot Nexus to fastboot with: adb reboot booloader
3. Unlock bootloader: fastboot oem unlock
4. Flash stock image to Nexus (cd into the directory where the stock image was unzipped to first): ./flash-all.sh
5. Reboot into the new stock image
6. Set up stock image (you can skip most of the configuration since we'll be wiping it soon)
7. Enable developer options in stock image
8. Enable USB debugging in developer settings and authorize your computer
9. Reboot Nexus to fastboot with: adb reboot booloader
10. Download modded MultiROM TWRP and modded MultiROM (https://basketbuild.com/devs/Captain_Throwback/Nexus%205/MultiROM)
11. Install modded TWRP recovery with: fastboot flash recovery /path/to/twrp/file
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
30. Reboot back into TWRP
31. Tap 3 bars in corner, then Add ROM, then choose the CM-Stripped ROM and install it
32. Reboot into the CM-Stripped ROM and give it about 5 minutes to let it boot (It will be at the Google logo)
33. On your computer, restart adb as root: adb root
34. Run the Plasma Mobile flashing script on your computer (make sure the Nexus is connected of course) (if needed chmod +x the script)
35. Once the script is finished, the Nexus will reboot and if you don't catch it in time it will boot to Lineage. If it does just reboot back into cm-stripped
36. Test out Plasma Mobile, make sure it boots (Plasma Mobile is still in a developmental stage so a lot of stuff is broken right now)
37. Reboot back to TWRP
38. Flash SuperSU (https://download.chainfire.eu/1021/SuperSU/SR3-SuperSU-v2.79-SR3-20170114223742.zip)
39. Reboot back to LineageOS
40. Install the modded .apk of MultiROM Manager (the Ubports version)
41. Reboot back to TWRP
42. Install standard MultiROM (https://forum.xda-developers.com/google-nexus-5/orig-development/mod-multirom-v24-t2571011)
43. Reboot back to LineageOS
44. From MultiROM Manager, install Ubuntu Touch (stable version 13 is what I use). Reboot into recovery when asked.
45. Boot Ubuntu Touch to make sure the install worked
46. Reboot to fastboot
47. Download MultiROM TWRP (https://forum.xda-developers.com/google-nexus-5/orig-development/mod-multirom-v24-t2571011)
48. Flash MultiROM TWRP to Nexus: fastboot flash recovery /path/to/twrp
49. Boot into TWRP and add a ROM of type Sailfish OS
50. Select the CM11 Snapshot M11 zip as the CyanogenMod zip and the Sailfish zip as the rootfs zip
51. Boot SailfishOS to make sure it works
52. Reboot into fastboot bootloader
53. Flash Updated TWRP For Nougat ROM Compatibility (https://www.androidfilehost.com/?w=files&flid=102780)
54. Reboot back into LineageOS and uninstall the both the Google Play version and the old Ubports version of MultiROM Manager. Install the new Ubports version located here: (https://forum.xda-developers.com/showpost.php?p=71471699&postcount=3668). 
55. Reboot back into TWRP
56. Add a new ROM in MultiROM Settings
57. Select the CyanogenMod 11 .zip
58. Set the image sizes: 436MB for cache, 4095MB for data, 512MB for system
59. Swipe to confirm and install the ROM.