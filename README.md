# osx

currently running Macos x 10.13.2 on the asus gl702vm i5 with BIOS 306
please update Bios to 306 to use the Acpi Files.

remove appleintellpssi2c.kext's and applehpm.kext for touchpad to work.
Fn keys
volume F10 F11 F12
backlight FN+ Pause/break FN+ Page up, brightness slider


things that don't work:
keyboard backlight 


notes:

Sierra 10.13.2

High Sierra 10.13.3 works but theres Graphics issues with the latest Nvidia Drivers. 
onboard 1 hda gfx must be the same for both gfx0 and hdau for hdmi audio to work. 
this repo has acpi patches so you can build your own dsdt. 
i would reccomend you use the hack-ssdt's not named SSDT-0/4 the setup depends on them to be there. 
apply the patches in order after installing rehabmans maciasl and updating iasl to the latest 6.x. 
following his guide to extract and decompile with refs.txt. 
SSDT-1 in the ACPI-patches.zip should replace the one from your system as it wont compile and needs lots of work.

BACKLIGHT.
to have a working native backlight with gtx1060 you need to copy your vanilla AppleBacklight.kext
to: /OTHER/PatchAppleBacklight/Vanilla and run the Patch.sh and install it to system/library/Extensions/
i have included my kexts but your screen may be made by a different vendor so you may need to apply this to have working backlight

NOTE: the screen Backlight will be black when first booted up, its a bug i need to fix, just Turn the Brightness up From the keyboard
