# Guía de instalación de H12

Esta guía es una traducción automática; las correcciones son bienvenidas a través de GitHub Issues.

H12 es un proyecto de fans gratuito basado en el motor fheroes2, bajo licencia GPL-2.0-or-later; no está afiliado a Ubisoft ni a New World Computing, y "Heroes of Might and Magic" es una marca comercial de sus propietarios. La versión 1.0.0-beta.1 es una BETA, por lo que usted se encuentra entre sus primeros evaluadores humanos: ¡gracias por sus informes!

## Qué necesita

Necesita su propio Heroes of Might and Magic II; se recomienda la edición GOG Gold, y Price of Loyalty es opcional. Para el modo Heroes I, también necesita su propio Heroes of Might and Magic, también a la venta en GOG. H12 no incluye archivos originales del juego.

## Windows

**Paso 1.** Descargue `H12-1.0.0-beta.1-windows-x64.zip` de la página de lanzamientos.

**Paso 2.** Extraiga todo el ZIP en una carpeta con permisos de escritura como `C:\Games\H12`, manteniendo todo junto.

**Paso 3.** Copie las carpetas `DATA`, `MAPS`, `MUSIC` y `ANIM` de Heroes II junto a `H12.exe`. Windows fusiona `DATA` con la carpeta `data` existente: conserve sus subcarpetas PNG. Se requiere `DATA/HEROES2.AGG`; `DATA/HEROES2X.AGG` añade Price of Loyalty.

**Paso 4.** Para el modo Heroes I, copie `DATA\HEROES.AGG` y `HEROES.EXE` en `DATA`. H12 solo lee `HEROES.EXE` como datos; nunca lo ejecuta.

**Paso 5.** De forma opcional, copie `homm1.gog` en `DATA` para la música y el vídeo de Heroes I, y copie `MAPS\*.MAP` y `*.CMP` en `MAPS`; H12 convierte esos mapas automáticamente.

Su carpeta terminada se verá así:

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

**Paso 6.** Inicie `H12.exe`. Es posible que Windows muestre una advertencia de SmartScreen porque el programa no está firmado. La configuración, las partidas guardadas y el registro están en `%APPDATA%\fheroes2`, compartidos con el fheroes2 estándar.

## Android

**Paso 1.** Descargue `H12-1.0.0-beta.1.apk` de la página de lanzamientos e instálelo. Permita los orígenes desconocidos cuando se le solicite; H12 no necesita permisos de internet.

**Paso 2.** En un ordenador, cree un archivo ZIP de su carpeta de Heroes II que contenga `DATA/HEROES2.AGG`. Price of Loyalty se incluye automáticamente si está presente.

**Paso 3.** Para el modo Heroes I, cree un segundo archivo ZIP de su carpeta de Heroes of Might and Magic que contenga `DATA/HEROES.AGG` y `HEROES.EXE`. `MAPS` y `homm1.gog` son opcionales. Cada archivo ZIP ocupa unos 400 MB.

**Paso 4.** Copie el archivo ZIP o ambos archivos ZIP en su teléfono, por ejemplo en Downloads.

**Paso 5.** Abra H12.

![Android antes de cargar](images/android-01-no-data.png)

**Paso 6.** Toque "LOAD DATA FROM A ZIP" y seleccione el ZIP de Heroes II. Espere uno o dos minutos con la pantalla encendida; repita para el ZIP de Heroes I.

![Datos cargados en Android](images/android-04-all-loaded.png)

**Paso 7.** Toque "START GAME" cuando Heroes 2 esté cargado. Utilice "SAVED GAMES" para gestionar las partidas guardadas.

## Primer inicio, modos de juego y castillos

**Paso 1.** Elija un idioma en "Select Game Language:"; el inglés viene preseleccionado. En una pantalla táctil, una pulsación prolongada seguida de un segundo toque funciona como un clic derecho.

**Paso 2.** Abra los ajustes desde el menú principal: seleccione la puerta de la casa a la izquierda en Heroes II, o la torre izquierda del castillo en Heroes I. En un PC, presione `T` en su lugar.

![Ajustes del juego](images/game-03-settings-mode2.png)

**Paso 3.** Utilice "Game Version" para cambiar entre Heroes 2 y Heroes 1. El juego recuerda su elección. Sin los archivos de Heroes I, muestra "Heroes 1 data required" y permanece en Heroes II.

**Paso 4.** Abra "Extra Castles" en los ajustes y active los castillos que desee. Están en Off por defecto. Heroes II ofrece Oasis, Inferno, Hive y Atoll; Heroes I también ofrece Wizard y Necromancer.

![Castillos adicionales](images/game-05-extra-castles-mode2.png)

**Paso 5.** Elija "NEW GAME" -> "STANDARD GAME". En Heroes II, toque la imagen debajo de "Class:"; las clases fijas aparecen en gris, así que pruebe "Pandemonium" o "Broken Alliance". En Heroes I, toque el jinete debajo de "Choose Color:" para elegir entre un máximo de diez castillos.

![Elección de castillos](images/game-12-castle-choice-mode1.png)

## Informar de problemas

Envíe sus informes a https://github.com/h12-game/h12/issues o a h12.uniformed930@slmails.com. Incluya la versión 1.0.0-beta.1, PC o Android, modo I o II, si Price of Loyalty está instalado, los pasos para reproducir el problema, el registro y una partida guardada si procede.

En PC, el registro se encuentra en `%APPDATA%\fheroes2\fheroes2.log` y las partidas guardadas están en `%APPDATA%\fheroes2\files\save`. Android escribe en el registro del sistema (`logcat`) bajo la etiqueta `fheroes2`.

Los GitHub Issues son públicos. Los correos electrónicos pasan a través de un servicio de alias hacia un buzón ordenado por un asistente automatizado (IA); se conservan durante un máximo de 12 meses y el spam se elimina transcurridos 30 días.

## Pequeños problemas conocidos

- En Heroes II, "Extra Castles" puede mostrar "Oasis + Inferno" incluso cuando Hive y Atoll estén en On. Abra la ventana para ver su estado real.
- "Heroes 1 data required" solo menciona `HEROES.AGG`, pero el modo Heroes I necesita tanto `HEROES.AGG` como `HEROES.EXE`.
