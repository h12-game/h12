# H12 1.0.0-beta.1

H12 is a fan project based on the fheroes2 engine (GPL-2.0-or-later), not affiliated with Ubisoft or New World Computing. Heroes of Might and Magic is a trademark of its owner.

## Beta test

This is a beta test. The alpha test was done mainly by AI through automated games and headless checks, so players are among the first human testers. Thank you for every report.

## What is new

Heroes 1 mode includes the Wizard and Necromancer castles. Heroes 2 mode adds Oasis, Inferno, Hive and Atoll. Heroes 1 maps are converted in the game from the player's own copy.

## Requirements

You must own Heroes of Might and Magic II (GOG Gold recommended; Price of Loyalty optional). For Heroes 1 mode you must also own Heroes of Might and Magic I. No original game data are included. Without the player's Heroes II data the game does not start; Heroes I mode additionally requires the player's Heroes I data.

## Downloads

- [Windows x64](https://github.com/h12-game/h12/releases/download/v1.0.0-beta.1/H12-1.0.0-beta.1-windows-x64.zip)
- [Android APK](https://github.com/h12-game/h12/releases/download/v1.0.0-beta.1/H12-1.0.0-beta.1.apk)
- [Complete corresponding source](https://github.com/h12-game/h12/releases/download/v1.0.0-beta.1/H12-1.0.0-beta.1-source.zip)
- [SHA-256 checksums](https://github.com/h12-game/h12/releases/download/v1.0.0-beta.1/SHA256SUMS.txt)

The corresponding source is provided with every release under the GPL. This small web-upload repository contains release documentation; the complete source is the source ZIP linked above.

## Feedback and privacy

Please report the version, PC or Android, mode I or II, whether Price of Loyalty is installed, steps to reproduce, a log and, if relevant, a saved game.

Use [GitHub Issues](https://github.com/h12-game/h12/issues) or email [h12.uniformed930@slmails.com](mailto:h12.uniformed930@slmails.com). Emails are forwarded by an alias service to a mailbox where an automated assistant (AI) sorts them. GitHub Issues are public.
Emails are kept for at most 12 months; messages held as spam are deleted after 30 days.

## Building from source

PC: use CMake as for [upstream fheroes2](https://github.com/ihhub/fheroes2), with SDL2, SDL2_mixer and zlib. The Windows release uses the llvm-mingw x64 cross compiler and file-prefix mapping to remove build paths. Android: use Gradle in `android`, with the Android SDK/NDK and the SDL sources. For a public build set `FHEROES2_APPLICATION_ID=cz.h12.hra`, `FHEROES2_APP_LABEL=H12`, `FHEROES2_VERSION_NAME=1.0.0-beta.1`, `FHEROES2_VERSION_CODE=10000`, `FHEROES2_FAZE=beta`, and the feedback settings above; leave `FHEROES2_PC_URL` unset. Signing credentials are supplied separately and are never included.

## Documentation and credits

Installation guide (Windows, Android, switching between Heroes I and Heroes II, new castles): [English](docs/INSTALL.md), [German](docs/INSTALL.de.md), [Spanish](docs/INSTALL.es.md), [Czech](docs/INSTALL.cs.md). The translations are machine translations; corrections are welcome. See [docs](docs/README.md).

Thanks to the fheroes2 team and upstream contributors. See LICENSE and THIRD_PARTY_LICENSES.md for licensing information.
