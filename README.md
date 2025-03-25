# Sat Moons
version 4\
xhul - 2025\
download: https://github.com/xhul-dev/Sat_Moons/releases
\
reports: https://github.com/xhul-dev/Sat_Moons/issues

## description

Sat Moons is a compilation of homebrews for the Sega Saturn, using Atlas multi-boot capability.\
It's obviously aimed at people who still use actual CDs, though it should work from any ODE as well.\
Its usefulness aside, the project is a tribute to the wonderful Atlas software.

So far, it includes the following:
- Artemio's 240p Test Suite 0.1
- Memory Map Viewer
- SDLoader 0.127d, 0.381
- Save Game Copier 3.6.18 - 332 saves total
- Save Game Extractor 0.99
- Save Game Manager 5 - 45 firmwares total
- Save To QR Code 1.000

At the main screen, [A] shows information for the active entry (features or things to know).\
Feel free to let me know if something doesn't work as expected.\
Suggestions are also welcome, especially other stuff worth injecting.

Things i wanted to inject, but won't:
- Save Data Manager - significant incompatibility with Atlas

## documentation - Atlas

version 05/12/04\
by The Rockin'-B\
original documentation: \\README\\ATLAS.TXT\
web: http://www.rockin-b.de/saturn-atlascreator.html

Changes since the original release:
- The main and credits screens, as well as the CD icon, were customised for Sat Moons.
- The audio track file was converted from .mp3 to .wav, for compatibility purpose.

Known issues:
- Info screens automatically close if auto rotate is on, disabling it first solves the problem.

## documentation - Artemio's 240p Test Suite

version 0.1\
by Artemio Urbina, hitomi2500\
entry location: \\01ATS\\\
original documentation: \\README\\ATS.TXT\
web: https://github.com/hitomi2500/240pTestSuite

## documentation - Memory Map Viewer

by Charles MacDonald\
entry location: \\02MMV\\\
original documentation: \\README\\MMV.TXT\

Known issues:
- [START] freezes the software (probably because it's executed from Atlas).

## documentation - SDLoader

version 0.127d, 0.381\
by Murzik\
entry location: \\03SDL1\\, \\04SDL2\\\
original documentation: \\README\\SDL1.TXT, \\README\\SDL2.TXT\
web: https://segaxtreme.net/threads/sdloader-v0-12-run-binaries-from-sd-card-and-backup-restore-saves.25275/

For compatibility purpose, SDL uses 2 Atlas entries:
- version 0.127d
- version 0.381

Version 0.381 includes more features, but it's not directly compatible with all machines.\
If "SD card init error" is displayed when attempting to read|write from|to the card, you have to use 0.127d instead.\
The cool part is that executing 0.381 from 0.127d solves the compatibility issue.

Executing 0.381 from 0.127d, to access all features:
- Make sure the card is formatted to FAT16 or FAT32.
- Make sure 0.381 is on the card as BOOT.BIN (available in \\03SDL1\\SDCARD\\).
- Execute 0.127d from Sat Moons.
- Execute BOOT.BIN from the SDL main menu (if "SD card init error" is displayed, a second attempt is required).
- Enjoy 0.381.

Technically, 0.381 also supports exFAT, but you can use that file system only if your machine doesn't require the 0.127d trick.

Available in \\04SDL2\\SDCARD\\:
- RAMEMPTY.BIN:\
Select that file for restoration to reset the internal save memory from the software.\
Basically the same as using "Clear" from the BIOS memory management.
- ROMEMPTY.BIN:\
Select that file for restoration to reset the cartridge save memory from the software.\
Basically the same as using "Clear" from the BIOS memory management.\
Compatible with cartridges that allow hardware direct save (official ones, some all-in-one variants, etc.).
- CODE.CFG:\
The identification, load and start addresses of the code to execute.\
It's provided as an example, the file name can be anything (as long as it's a .CFG).\
When a (non-CFG) file is executed directly instead, the default is 0x06004000 for both addresses.

If you're looking for a specific cartridge firmware to put on the SD card, there's a collection available in \\08SGM\\FIRMWARE\\.\
The flashing is at your own risk, of course.

Known issues:
- "SD card init error" on some machines, see above.

## documentation - Save Game Copier

version 3.6.18\
by slinga\
entry location: \\05SGC1\\, \\06SGC2\\\
original documentation: \\README\\SGC.TXT\
web: https://github.com/slinga-homebrew/Save-Game-Copier

Because it can't access more than 254 saves in \\SATSAVES\\, SGC uses 2 Atlas entries:
- saves from A to M
- saves from N to Z

Changes since the original release:
- Many saves were added.
- The eighth character of each .BUP name is now always used to differentiate saves with identical internal names (A, B, and so on).
- The existing .BUP files were renamed to match the new format.
- The save documentation is now to be found in \\SAVEINFO\\:
  - \_\_\_\_LIST.TXT includes general info, and basically replaces \\SATSAVES\\CREDITS.TXT.
  - Other files whose names start with \_ cover multiple saves from the same author.
  - Other files whose names match a .BUP cover that specific save only.

Known issues:
- It can take a while before the list of saves on the CD is displayed for the first time (around 0.13 seconds per save).
- "Exit to CD Player" freezes the software (probably because it's executed from Atlas).

## documentation - Save Game Extractor

version 0.99\
by slinga\
entry location: \\07SGE\\\
original documentation: \\README\\SGE.TXT\
web: https://github.com/slinga-homebrew/Save-Game-Extractor

## documentation - Save Game Manager

release 5\
by The Rockin'-B\
entry location: \\08SGM\\\
original documentation: \\README\\SGM.TXT\
web: http://www.rockin-b.de/saturn-rb-all-stars.html

If you intend to use SGM for cartridge firmware flashing (at your own risk), they're located in \\08SGM\\FIRMWARE\\.\
Note that if you own an SDLoader module, the SDLoader software does it much faster.

Changes since the original release:
- The Atlas sprite and info screen were customised for Sat Moons.
- The Atlas text description is now more straightforward, to reduce clutter.
- The Atlas audio file was removed, to reduce creepyness.
- The background is now fully black, for readability purpose.
- Many firmwares were added.

Known issues:
- The explorer can't access more than 25 files|directories (including . and ..) in the root of the CD.
- "rescan" freezes the software (probably because it's executed from Atlas).

## documentation - Save To QR Code

version 1.000\
by Ervilsoft\
entry location: \\09SQR\\\
original documentation: \\README\\SQR.TXT\
web: https://segaxtreme.net/threads/sega-saturn-28th-anniversary-game-competition.25278/page-2#post-183550

Known issues:
- At the main screen, the available options don't do anything if no saves are present on the corresponding device.
- "Exit" freezes the software (probably because it's executed from Atlas).
- [A+B+C+START] freezes the software (probably because it's executed from Atlas).

## history

### version 4

- The project, now called Sat Moons, is no longer limited to just utilities.
- The main background is significantly less dull.
- The entry sprites are now smaller spheres without rings.
- The CD icon was updated to match the new project name.
- Known issues have been added to the documentation.

### version 3

- Memory Map Viewer has joined forces!
- The CD IP is now more conventional, for compatibility purpose.

### version 2

- Save To QR Code has joined forces!
- The Atlas info screens for Save Game Extractor and Save Game Manager were improved.
- The Atlas sprites are cooler now.

### version 1

- Initial release, 7 Atlas entries.

## credits

- Artemio Urbina - Artemio's 240p Test Suite
- Charles MacDonald - Memory Map Viewer
- Ervilsoft - Save To QR Code
- Murzik - SDLoader
- The Rockin'-B - Atlas, Save Game Manager
- hitomi2500 - Artemio's 240p Test Suite
- slinga - Save Game Copier, Save Game Extractor
