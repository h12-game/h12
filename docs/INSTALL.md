# H12 installation guide

Welcome to H12 (version 1.0.0-beta.1). H12 is a fan project based on the fheroes2 engine and is released under the GPL-2.0-or-later license. It is not affiliated with Ubisoft or New World Computing. "Heroes of Might and Magic" is a trademark of its respective owners.

This release is a BETA version. The alpha test was carried out mainly by artificial intelligence through automated games and automated tests without a game window. Because of this, you are among the very first human testers to play H12. Thank you for every bug report and suggestion you send us! If you find any issues or want to share feedback, please see the [Reporting problems](#reporting-problems) section at the end of this guide.

This guide explains how to install H12 on Windows and Android, how to switch between Heroes 1 and Heroes 2 mode, and how to turn on the new castles. It is not a guide on how to play the game itself.

## What you need

No original game files are included in H12, and the game cannot start without your own files.

* **For both modes (Heroes II and Heroes I):** You need your own copy of Heroes of Might and Magic II. We recommend the Gold edition from GOG. The Price of Loyalty expansion is optional.
* **For Heroes 1 mode (optional):** You also need your own copy of the first Heroes of Might and Magic game, which is also sold on GOG.

## Windows (PC)

Follow these steps to install and run H12 on a Windows PC:

1. Download `H12-1.0.0-beta.1-windows-x64.zip` from the release page.
2. Extract the complete ZIP archive into a writable folder on your computer, for example `C:\Games\H12`. Make sure to keep `H12.exe`, all six DLL files (`SDL2.dll`, `SDL2_mixer.dll`, `libz.dll`, `libc++.dll`, `libunwind.dll`, `libwinpthread-1.dll`), the `files` folder, and the `data` folder together in the same place.
3. **Add Heroes II files (required):** Open your original Heroes II installation folder. Copy the contents of the `DATA`, `MAPS`, `MUSIC`, and `ANIM` folders into folders with the same names right next to `H12.exe` (create these folders if needed).
   * `DATA/HEROES2.AGG` is required to start the game.
   * `DATA/HEROES2X.AGG` is optional and enables Price of Loyalty content.
   * Keep the packaged PNG subfolders inside `data/`. Windows treats `DATA` and `data` as the same folder, so your copied `DATA` files go directly into that existing folder alongside the PNG subfolders.
4. **Add Heroes I files (optional, for mode I):** Open your original Heroes of Might and Magic folder and copy the following files into your H12 folder:
   * Copy `DATA\HEROES.AGG` to `DATA\HEROES.AGG` (required for mode I).
   * Copy `HEROES.EXE` to `DATA\HEROES.EXE` (required for mode I; this file is only read as data and is never run).
   * Copy `homm1.gog` to `DATA\homm1.gog` (optional; adds Heroes I music and video).
   * Copy the original map files `MAPS\*.MAP` and `MAPS\*.CMP` into the `MAPS\` folder next to `H12.exe` (optional; adds Heroes I scenarios, which H12 converts automatically).
5. Start the game by running `H12.exe`. Windows may show a SmartScreen warning because the program is not signed.

Here is how your folder looks right after extracting the H12 ZIP archive, and how it looks after adding your original game files:

```text
BEFORE (extracted from H12-1.0.0-beta.1-windows-x64.zip):
C:\Games\H12\
├── H12.exe
├── SDL2.dll
├── SDL2_mixer.dll
├── libz.dll
├── libc++.dll
├── libunwind.dll
├── libwinpthread-1.dll
├── files\
└── data\
    └── (packaged PNG subfolders)

AFTER (with Heroes II and Heroes I files copied in):
C:\Games\H12\
├── H12.exe
├── SDL2.dll
├── SDL2_mixer.dll
├── libz.dll
├── libc++.dll
├── libunwind.dll
├── libwinpthread-1.dll
├── files\
├── DATA\ (same folder as data\)
│   ├── (packaged PNG subfolders)
│   ├── HEROES2.AGG
│   ├── HEROES2X.AGG         (optional, Price of Loyalty)
│   ├── HEROES.AGG           (required for mode I)
│   ├── HEROES.EXE           (required for mode I, read as data only)
│   └── homm1.gog            (optional, Heroes I music and video)
├── MAPS\
│   ├── (Heroes II maps)
│   └── (*.MAP and *.CMP files from Heroes I)
├── MUSIC\
│   └── (Heroes II music files)
└── ANIM\
    └── (Heroes II animation files)
```

Your settings, saved games, and log file are stored in `%APPDATA%\fheroes2`:
* Saved games: `%APPDATA%\fheroes2\files\save`
* Log file: `%APPDATA%\fheroes2\fheroes2.log`

This is the exact same folder that the standard fheroes2 engine uses. If you also use fheroes2 on your PC, both programs share this folder.

## Android

Follow these steps to install H12 and load your game data on Android:

1. Download `H12-1.0.0-beta.1.apk` from the release page and install it on your phone. Allow installing apps from unknown sources when your phone asks. The app needs no internet permission.
2. On a computer, create a ZIP file from your Heroes II game folder. It must contain `DATA/HEROES2.AGG`. If `DATA/HEROES2X.AGG` is inside the ZIP, Price of Loyalty is included automatically.
3. If you want to play mode I, create a second ZIP file from your Heroes of Might and Magic folder. It must contain `DATA/HEROES.AGG` and `HEROES.EXE`. Including the `MAPS` folder (with `.MAP` and `.CMP` files) and `homm1.gog` is optional. Each ZIP file is about 400 MB, so make sure your phone has enough free space.
4. Copy the ZIP file (or both ZIP files) to your phone, for example into the `Downloads` folder.
5. Open H12 on your phone. The start screen says `"The game needs the data of your own copy."` and shows a `"Loaded:"` status list (`Heroes 2`, `Price of Loyalty`, `Heroes 1`, `Heroes 1 maps`, `homm1.gog`). The `"START GAME"` button is disabled until `Heroes 2` is loaded. The start screen also shows the feedback links.

![Android start screen without data](images/android-01-no-data.png)

6. Tap `"LOAD DATA FROM A ZIP"` and choose your Heroes II ZIP file in the file picker.

![Choosing the game ZIP in the Android file picker](images/android-02-choose-zip.png)

7. Wait while the game unpacks the archive. Unpacking takes a minute or two; please keep the screen open. When it finishes, the screen shows `"Heroes 2: yes"` (and `"Price of Loyalty: yes"` if included).

![Android start screen with Heroes 2 loaded](images/android-03-heroes2-loaded.png)

8. For mode I, tap `"LOAD DATA FROM A ZIP"` again and choose your Heroes I ZIP file. Loading the second ZIP does not remove what the first one installed. Once complete, all five lines say `"yes"`.

![Android start screen with all data loaded](images/android-04-all-loaded.png)

9. Tap `"START GAME"` to launch H12. You can also manage your saved games from this screen by tapping `"SAVED GAMES"`.

## First start

When you start the game for the first time, it asks you to choose a language under `"Select Game Language:"`. English is preselected.

![Language selection on first start](images/game-01-language.png)

After you confirm the language, a short welcome message appears. It explains that on touch screens, a long touch followed by a second touch simulates a right-click.

## Switching between Heroes II and Heroes I

You can switch between Heroes II (mode II) and Heroes I (mode I) in the game settings, which you open from the main menu. The game remembers your chosen mode for the next start.

1. In the Heroes II main menu, open the game settings by tapping (or clicking) the door of the house on the left. You can also tap `"SETTINGS"` in the `"NEW GAME"` menu of Heroes II, or press `T` in the main menu on a PC.

![Heroes II main menu](images/game-02-main-menu-mode2.png)

2. In the settings window, look for `"Game Version"`. It shows `"Heroes 2"` or `"Heroes 1"`. Tap (or click) it to switch between the two modes.

![Settings in mode II](images/game-03-settings-mode2.png)

![Settings switched to Heroes 1](images/game-07-settings-mode1.png)

3. If you try to switch to `"Heroes 1"` without having the required Heroes I files installed, the game shows the message `"Heroes 1 data required"` and stays in Heroes II mode.

![Heroes 1 data required message](images/game-04-heroes1-data-required.png)

4. When you switch to mode I, the main menu changes to look like the original Heroes of Might and Magic.

![Heroes I main menu](images/game-09-main-menu-mode1.png)

5. To open the settings while you are in the mode I main menu, tap (or click) the left tower of the castle, or press `T` on a PC.

![Opening settings from the Heroes I main menu](images/game-10-settings-from-mode1-menu.png)

## New castles

H12 includes new castles that are turned `Off` by default. You can enable them in the game settings:

1. Open the settings and tap `"Extra Castles"`.
2. In mode II, the window offers four new castles: `Oasis`, `Inferno`, `Hive`, and `Atoll`. Tap a castle name to switch it `On` or `Off`.

![Extra Castles window in mode II](images/game-05-extra-castles-mode2.png)

3. In mode I, the `"Extra Castles"` window additionally offers `Wizard` and `Necromancer`, giving you 6 extra castles in total. Tap any name to switch it `On` or `Off`.

![Extra Castles window in mode I](images/game-08-extra-castles-mode1.png)

Once enabled, you can pick the new castles when starting a standard game:

* **In mode II:** Go to `"NEW GAME"` -> `"STANDARD GAME"` and choose a scenario with `"SELECT"`. Under `"Class:"`, tap your class picture to cycle through all available classes, including the new castles. Note that some maps have fixed classes (shown as a gray picture). To try the new castles, choose a map whose class can be changed, for example `"Pandemonium"` or `"Broken Alliance"`.

![Choosing a class in mode II](images/game-06-castle-choice-mode2.png)

* **In mode I:** Go to `"NEW GAME"` -> `"STANDARD GAME"`. Under `"Choose Color:"`, tap the rider icon to cycle through all enabled castles (up to ten in total: Knight, Barbarian, Sorceress, Warlock, Oasis, Inferno, Hive, Atoll, Wizard, and Necromancer).

![New game screen in mode I](images/game-11-new-game-mode1.png)

![All ten castle choices in mode I](images/game-12-castle-choice-mode1.png)

Every castle has its own distinct town screen and look.

![Necromancer town in mode I](images/game-13-necromancer-town-mode1.png)

## Reporting problems

Thank you again for testing this beta and helping us improve H12! You can report bugs and send suggestions in two ways:

* **GitHub Issues:** https://github.com/h12-game/h12/issues
* **E-mail:** h12.uniformed930@slmails.com

When reporting a problem, please include the following details:
* Game version (`1.0.0-beta.1`)
* Platform (`PC` or `Android`)
* Active game mode (`mode I` or `mode II`)
* Whether `Price of Loyalty` is installed
* Clear steps to reproduce the problem
* The game log and, if relevant, a saved game file

**Where to find the log:**
* **PC:** The log file is saved at `%APPDATA%\fheroes2\fheroes2.log` (saved games are in `%APPDATA%\fheroes2\files\save`).
* **Android:** The game writes its log to the Android system log (`logcat`) under the tag `fheroes2`. It does not write a log file into the app folder.

**Privacy note:** GitHub Issues are public. If you send an e-mail, messages are forwarded by an alias service to a mailbox where an automated assistant (AI) sorts them. E-mails are kept for at most 12 months, and messages held as spam are deleted after 30 days.

## Known small issues in this beta

* In mode II, the `"Extra Castles"` label in the main settings window may say `"Oasis + Inferno"` even when `Hive` and `Atoll` are also turned `On`. Open the `"Extra Castles"` window to see the real state of each castle.
* The `"Heroes 1 data required"` message names only `HEROES.AGG`, but mode I actually requires both `HEROES.AGG` and `HEROES.EXE`.
