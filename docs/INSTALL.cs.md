# Průvodce instalací H12

Tento návod je strojový překlad; opravy jsou vítány přes GitHub Issues.

H12 je bezplatný fanouškovský projekt založený na enginu fheroes2, licencovaný pod GPL-2.0-or-later; nemá žádnou spojitost se společnostmi Ubisoft ani New World Computing a "Heroes of Might and Magic" je ochranná známka jejích vlastníků. Verze 1.0.0-beta.1 je BETA, takže patříš mezi její první lidské testery: děkujeme za tvá hlášení!

## Co budeš potřebovat

Potřebuješ vlastní Heroes of Might and Magic II; doporučuje se edice Gold z GOGu a Price of Loyalty je volitelné rozšíření. Pro režim Heroes I potřebuješ také vlastní Heroes of Might and Magic, které se rovněž prodávají na GOGu. H12 neobsahuje žádné původní herní soubory.

## Windows

**Krok 1.** Stáhni si `H12-1.0.0-beta.1-windows-x64.zip` ze stránky vydání.

**Krok 2.** Rozbal celý ZIP do složky s právem zápisu, například `C:\Games\H12`, a nech všechno pohromadě.

**Krok 3.** Zkopíruj složky `DATA`, `MAPS`, `MUSIC` a `ANIM` ze hry Heroes II vedle `H12.exe`. Windows sloučí `DATA` s existující složkou `data`: podsložky s PNG v ní ponech. Soubor `DATA/HEROES2.AGG` je vyžadován; `DATA/HEROES2X.AGG` přidává Price of Loyalty.

**Krok 4.** Pro režim Heroes I zkopíruj `DATA\HEROES.AGG` a `HEROES.EXE` do `DATA`. H12 čte `HEROES.EXE` pouze jako data; nikdy ho nespouští.

**Krok 5.** Volitelně můžeš do `DATA` zkopírovat `homm1.gog` pro hudbu a videa z Heroes I a do `MAPS` zkopírovat `MAPS\*.MAP` a `*.CMP`; H12 tyto mapy převede automaticky.

Tvoje výsledná složka bude vypadat takto:

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

**Krok 6.** Spusť `H12.exe`. Windows může zobrazit varování funkce SmartScreen, protože program není podepsaný. Nastavení, uložené pozice a záznam protokolu jsou v `%APPDATA%\fheroes2`, sdílené se standardním fheroes2.

## Android

**Krok 1.** Stáhni si `H12-1.0.0-beta.1.apk` ze stránky vydání a nainstaluj ho. Pokud se systém zeptá, povol neznámé zdroje; H12 nepotřebuje žádná oprávnění k internetu.

**Krok 2.** Na počítači vytvoř ZIP archiv své složky Heroes II obsahující `DATA/HEROES2.AGG`. Price of Loyalty se zahrne automaticky, pokud je k dispozici.

**Krok 3.** Pro režim Heroes I vytvoř druhý ZIP archiv složky Heroes of Might and Magic obsahující `DATA/HEROES.AGG` a `HEROES.EXE`. `MAPS` a `homm1.gog` jsou volitelné. Každý ZIP má zhruba 400 MB.

**Krok 4.** Zkopíruj ZIP nebo oba ZIPy do telefonu, například do složky Downloads.

**Krok 5.** Otevři H12.

![Android před načtením](images/android-01-no-data.png)

**Krok 6.** Klepni na "LOAD DATA FROM A ZIP" a vyber ZIP s Heroes II. Počkej minutu nebo dvě se zapnutou obrazovkou; totéž zopakuj pro ZIP s Heroes I.

![Android s načtenými daty](images/android-04-all-loaded.png)

**Krok 7.** Jakmile se Heroes 2 načte, klepni na "START GAME". Pro správu uložených her použij "SAVED GAMES".

## První spuštění, herní režimy a hrady

**Krok 1.** Vyber jazyk v nabídce "Select Game Language:"; předvolená je angličtina. Na dotykové obrazovce funguje dlouhý stisk následovaný druhým dotykem jako kliknutí pravým tlačítkem myši.

**Krok 2.** Otevři nastavení z hlavní nabídky: v Heroes II vyber dveře domku vlevo, v Heroes I levou věž hradu. Na PC můžeš místo toho stisknout `T`.

![Nastavení hry](images/game-03-settings-mode2.png)

**Krok 3.** Pomocí "Game Version" přepínej mezi Heroes 2 a Heroes 1. Hra si tvoji volbu zapamatuje. Bez souborů pro Heroes I se zobrazí "Heroes 1 data required" a zůstaneš v Heroes II.

**Krok 4.** V nastavení otevři "Extra Castles" a zapni hrady, které chceš. Ve výchozím stavu jsou vypnuté. Heroes II nabízí Oasis, Inferno, Hive a Atoll; Heroes I navíc nabízí Wizard a Necromancer.

![Další hrady](images/game-05-extra-castles-mode2.png)

**Krok 5.** Zvol "NEW GAME" -> "STANDARD GAME". V Heroes II klepni na obrázek pod "Class:"; pevně dané třídy jsou šedé, tak vyzkoušej třeba "Pandemonium" nebo "Broken Alliance". V Heroes I klepni na jezdce pod "Choose Color:" a vyber si až z deseti hradů.

![Výběr hradů](images/game-12-castle-choice-mode1.png)

## Hlášení problémů

Hlášení posílej na https://github.com/h12-game/h12/issues nebo na h12.uniformed930@slmails.com. Uveď verzi 1.0.0-beta.1, zda jde o PC nebo Android, režim I nebo II, zda máš nainstalováno Price of Loyalty, postup k reprodukci chyby, log a případně i uloženou pozici.

Na PC najdeš log v `%APPDATA%\fheroes2\fheroes2.log` a uložené hry v `%APPDATA%\fheroes2\files\save`. Android zapisuje do systémového logu (`logcat`) pod značkou `fheroes2`.

GitHub Issues jsou veřejné. E-maily procházejí aliasovací službou do schránky, kterou třídí automatický asistent (AI); uchovávají se maximálně 12 měsíců a spam je mazán po 30 dnech.

## Známé drobné problémy

- V Heroes II může "Extra Castles" zobrazovat "Oasis + Inferno", i když jsou Hive a Atoll zapnuté. Otevři toto okno, abys viděl jejich skutečný stav.
- Hláška "Heroes 1 data required" zmiňuje pouze `HEROES.AGG`, ale režim Heroes I vyžaduje jak `HEROES.AGG`, tak `HEROES.EXE`.
