# Sat Tools
version 1\
xhul - 2025\
download: https://github.com/xhul-dev/Sat_Tools/releases
\
reports: https://github.com/xhul-dev/Sat_Tools/issues

## description

This is a multi-boot Atlas CD image, so far including the following:
- Artemio's 240p Test Suite 0.1
- SDLoader 0.127d, 0.381 (both versions for compatibility purpose)
- Save Game Copier 3.6.18 - 332 saves total
- Save Game Extractor 0.99
- Save Game Manager 5 - 45 firmwares total

It should be useful mostly to people who use at least 2 of those on a regular basis, from physical CDs.\
The project is also my own tribute to the wonderful Atlas software.\
Once at the main screen, pressing A allows to view which main features each software has to offer.\
Feel free to let me know if something doesn't work as expected.\
I wasn't able to test the functionality from any ODE, so i'm all ears.\
Suggestions are also welcome, especially other useful tools that could be injected.\
Before you ask, Save Data Manager doesn't seem to work properly from Atlas, sadly.

## documentation - Atlas

by The Rockin'-B\
version 05/12/04\
original documentation: \README\ATLAS.TXT\
web: http://www.rockin-b.de/saturn-atlascreator.html

Changes since the original release:
- The main and credits screens, as well as the CD icon, were customised for Sat Tools.
- The audio track file was converted from .mp3 to .wav, for compatibility purpose.

## documentation - Artemio's 240p Test Suite

by Artemio Urbina, hitomi2500\
version 0.1\
entry location: \ATS\\\
web: https://segaxtreme.net/threads/sega-saturn-29th-anniversary-game-competition.25411/page-2#post-185171

It's the original release, without any modification.

## documentation - SDLoader

by Murzik\
version 0.127d, 0.381\
entry location (1 for each version): \SDL1\\, \SDL2\\\
web: https://segaxtreme.net/threads/sdloader-v0-12-run-binaries-from-sd-card-and-backup-restore-saves.25275/

Version 0.381 includes more features, but it's not directly compatible with all machines.\
If "SD card init error" is displayed when attempting to read|write from|to the card, you're concerned.\
Fortunately, 0.127d can be used to enable SPI mode on the card, after what 0.381 becomes fully functional.\
Here's the trick:
- Put 0.381 as BOOT.BIN on the card (provided in \SDL1\SDCARD\\).
- Execute 0.127d from Atlas.
- Execute BOOT.BIN from the SDL main menu.
  - On the first attempt, "SD card init error" is displayed, SPI mode is now (silently) enabled.
  - On the second attempt, 0.381 is successfully loaded, and can now communicate with the card properly.

Note about the card file system:\
FAT16 and FAT32 work with both versions.\
exFAT only works with 0.381, so you can't use it if the 0.127d trick is required.

Available in \SDL2\SDCARD\\:
- CODE.CFG:\
The identification, load and start addresses of the code to execute.\
It's provided as an example, the file name can be anything (as long as it's a .CFG).\
When a (non-cfg) file is executed directly instead, the default is 0x06004000 for both addresses.
- RAMEMPTY.BIN:\
Select that file for restoration to reset the internal save memory from the software.\
Basically the same as using "Clear" from the BIOS memory management.
- ROMEMPTY.BIN:\
Select that file for restoration to reset the cartridge save memory from the software.\
Basically the same as using "Clear" from the BIOS memory management.\
Compatible with cartridges that allow hardware direct save (official ones, some all-in-one variants, etc.).

If you're looking for a specific cartridge firmware to put on the card, there's a collection available in \SGM\FIRMWARE\ (at your own risk).

## documentation - Save Game Copier

by slinga\
version 3.6.18\
entry location (1 for each set of saves): \SGC1\\, \SGC2\\\
web: https://github.com/slinga-homebrew/Save-Game-Copier

Because SGC can't access more than 254 saves in \SATSAVES\\, they're separated by name (first character):
- A to M
- N to Z

Please note that it can take a while before the list of saves on the CD is displayed for the first time (around 0.13 seconds per save).

Changes since the original release:
- Many saves were added, the total is now 332.
- The eighth character of each .BUP is now always used to differentiate saves with identical internal names (A, B, and so on).
- The existing .BUP files were renamed to match the new format.
- The save documentation is now to be found in \SAVEINFO\\:
  - \_\_\_\_LIST.TXT includes general info, and basically replaces \SATSAVES\CREDITS.TXT.
  - .TXT files whose names start with \_ cover multiple saves from the same author.
  - .TXT files whose names match a .BUP cover that specific save only.

## documentation - Save Game Extractor

by slinga\
version 0.99\
entry location: \SGE\\\
web: https://github.com/slinga-homebrew/Save-Game-Extractor

It's the original release, without any modification.

## documentation - Save Game Manager

by The Rockin'-B\
release 5\
entry location: \SGM\\\
web: http://www.rockin-b.de/saturn-rb-all-stars.html

Changes since the original release:
- The Atlas sprite and info screen were customised for Sat Tools.
- The Atlas text description is now more straightforward, to reduce clutter.
- The Atlas audio file was removed, to reduce creepyness.
- The background is now fully black, for readability purpose.
- \FIRMWARE\ now includes a total of 45 256KB firmwares (at your own risk).

## history

### version 1

- Initial release, 7 Atlas entries.

## credits

- Artemio Urbina - Artemio's 240p Test Suite
- Murzik - SDLoader
- The Rockin'-B - Atlas, Save Game Manager
- hitomi2500 - Artemio's 240p Test Suite
- slinga - Save Game Copier, Save Game Extractor
