# osx

currently running Macos x 10.12.6 on the asus gl702vm i5 with BIOS 306
please update Bios to 306 to use the Acpi Files.

remove appleintellpssi2c.kext's and applehpm.kext for touchpad to work.
Fn keys
volume F10 F11 F12
backlight FN+ Pause/break FN+ Page up, brightness slider isnt functional but brightness works from brightness.app by berg Designs


things that don't work:
keyboard backlight 


notes:

Sierra 10.12.6

High Sierra 10.13.3 works but theres Graphics issues with the latest Nvidia Drivers. 
onboard 1 hda gfx must be the same for both gfx0 and hdau for hdmi audio to work. 
this repo has acpi patches so you can build your own dsdt. 
i would reccomend you use the hack-ssdt's not named SSDT-0/4 the setup depends on them to be there. 
apply the patches in order after installing rehabmans maciasl and updating iasl to the latest 6.x. 
following his guide to extract and decompile with refs.txt. 
SSDT-1 in the ACPI-patches.zip should replace the one from your system as it wont compile and needs lots of work.
