# osx

currently running Macos x 10.13.4 on the asus gl702vm i5 with BIOS 306
please update Bios to 306 to use the Acpi Files.

remove appleintellpssi2c.kext's and applehpm.kext for touchpad to work.
Fn keys
volume F10 F11 F12
backlight FN+ Pause/break FN+ Page up, brightness slider


things that don't work:
keyboard backlight.


notes:
High Sierra 10.13.4

onboard 1 hda gfx must be the same for both gfx0 and hdau for hdmi audio to work. 
this repo has acpi patches so you can build your own dsdt. 
i would reccomend you use the hack-ssdt's not named SSDT-0/4 the setup depends on them to be there. 
apply the patches in order after installing rehabmans maciasl and updating iasl to the latest 6.x. 
following his guide to extract and decompile with refs.txt. 
SSDT-1 in the patches folder should replace the one from your system as it wont compile and needs lots of work.

BACKLIGHT.
to have a working native backlight with gtx1060 you need to copy your vanilla AppleBacklight.kext
to: /OTHER/PatchAppleBacklight/Vanilla and run the Patch.sh and install the applebacklightinjector.kext to system/library/Extensions/
i have included my kexts but your screen may be made by a different vendor so you may need to make your own with the provided patcher to have working backlight.

NOTE: the screen Backlight was black when first booted up, i had to set brightness in config.plist

AppleGraphicsPowerManagment.kext:
to have better power managment on your gfx card you will need to edit the info.plist
look for your board-id ie: Mac-473D31EABEB93F9B, mine is mbp 13,2 smbios, and rename the graphics ie IGPU to GFX0 and copy the data from mbp 11,3 Mac-2BD1B31983FE1663 as it uses nvidia graphics.
i have included some prebuilt patched kexts for convenience.

