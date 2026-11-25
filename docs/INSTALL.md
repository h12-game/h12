# H12 installation guide

H12 is a free fan project based on the fheroes2 engine, licensed under GPL-2.0-or-later; it is not affiliated with Ubisoft or New World Computing, and "Heroes of Might and Magic" is a trademark of its owners. Version 1.0.0-beta.1 is a BETA, so you are among its first human testers: thank you for your reports!

## What you need

You need your own Heroes of Might and Magic II; the GOG Gold edition is recommended, and Price of Loyalty is optional. For Heroes I mode, you also need your own Heroes of Might and Magic, also sold on GOG. H12 includes no original game files.

## Windows

**Step 1.** Download `H12-1.0.0-beta.1-windows-x64.zip` from the release page.

**Step 2.** Extract the whole ZIP to a writable folder such as `C:\Games\H12`, keeping everything together.

**Step 3.** Copy the Heroes II `DATA`, `MAPS`, `MUSIC` and `ANIM` folders next to `H12.exe`. Windows merges `DATA` with the existing `data` folder: keep its PNG subfolders. `DATA/HEROES2.AGG` is required; `DATA/HEROES2X.AGG` adds Price of Loyalty.

**Step 4.** For Heroes I mode, copy `DATA\HEROES.AGG` and `HEROES.EXE` into `DATA`. H12 only reads `HEROES.EXE` as data; it never runs it.

**Step 5.** Optionally, copy `homm1.gog` into `DATA` for Heroes I music and video, and copy `MAPS\*.MAP` and `*.CMP` into `MAPS`; H12 converts those maps automatically.

Your finished folder will look like this:

```text
H12\
├── H12.exe, DLL files, files\
├── DATA\  (packaged PNG subfolders)
│   ├── HEROES2.AGG, HEROES2X.AGG
│   └── HEROES.AGG, HEROES.EXE, homm1.gog
├── MAPS\  (Heroes II and optional Heroes I maps)
├── MUSIC\
└── ANIM\
```

**Step 6.** Start `H12.exe`. Windows may show a SmartScreen warning because the program is not signed. Settings, saves and the log are in `%APPDATA%\fheroes2`, shared with standard fheroes2.

## Android

**Step 1.** Download `H12-1.0.0-beta.1.apk` from the release page and install it. Allow unknown sources when asked; H12 needs no internet permission.

**Step 2.** On a computer, make a ZIP of your Heroes II folder containing `DATA/HEROES2.AGG`. Price of Loyalty is included automatically if present.

**Step 3.** For Heroes I mode, make a second ZIP of your Heroes of Might and Magic folder containing `DATA/HEROES.AGG` and `HEROES.EXE`. `MAPS` and `homm1.gog` are optional. Each ZIP is about 400 MB.

**Step 4.** Copy the ZIP or both ZIPs to your phone, for example to Downloads.

**Step 5.** Open H12.

![Android before loading](images/android-01-no-data.png)

**Step 6.** Tap "LOAD DATA FROM A ZIP" and choose the Heroes II ZIP. Wait a minute or two with the screen on; repeat for the Heroes I ZIP.

![Android data loaded](images/android-04-all-loaded.png)

**Step 7.** Tap "START GAME" once Heroes 2 is loaded. Use "SAVED GAMES" to manage saves.

## First start, game modes and castles

**Step 1.** Choose a language at "Select Game Language:"; English is preselected. On a touch screen, a long touch followed by a second touch acts as a right-click.

**Step 2.** Open settings from the main menu: select the house door on the left in Heroes II, or the castle’s left tower in Heroes I. On a PC, press `T` instead.

![Game settings](images/game-03-settings-mode2.png)

**Step 3.** Use "Game Version" to switch between Heroes 2 and Heroes 1. The game remembers your choice. Without Heroes I files, it shows "Heroes 1 data required" and stays in Heroes II.

**Step 4.** Open "Extra Castles" in settings and turn on the castles you want. They are Off by default. Heroes II offers Oasis, Inferno, Hive and Atoll; Heroes I also offers Wizard and Necromancer.

![Extra castles](images/game-05-extra-castles-mode2.png)

**Step 5.** Choose "NEW GAME" -> "STANDARD GAME". In Heroes II, tap the picture under "Class:"; fixed classes appear gray, so try "Pandemonium" or "Broken Alliance". In Heroes I, tap the rider under "Choose Color:" to choose among up to ten castles.

![Castle choices](images/game-12-castle-choice-mode1.png)

## Reporting problems

Send reports to https://github.com/h12-game/h12/issues or h12.uniformed930@slmails.com. Include version 1.0.0-beta.1, PC or Android, mode I or II, whether Price of Loyalty is installed, steps to reproduce, the log and a saved game if relevant.

On PC, the log is `%APPDATA%\fheroes2\fheroes2.log` and saves are in `%APPDATA%\fheroes2\files\save`. Android writes to the system log (`logcat`) under the tag `fheroes2`.

GitHub Issues are public. Emails pass through an alias service to a mailbox sorted by an automated assistant (AI); they are kept at most 12 months, and spam is deleted after 30 days.

## Known small issues

- In Heroes II, "Extra Castles" may show "Oasis + Inferno" even when Hive and Atoll are On. Open the window to see their real state.
- "Heroes 1 data required" names only `HEROES.AGG`, but Heroes I mode needs both `HEROES.AGG` and `HEROES.EXE`.
