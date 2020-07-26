# DGUS-reloaded

Firmware for 3D printers' DGUS touchscreens.

The printer firmware to run alongside this can be found in [this repository](https://github.com/Desuuuu/Marlin).

## Disclaimer
**This software is provided without any warranty. You are solely responsible for your use of it.**

## Features

This firmware was inspired by Creality printers' touchscreen firmware. Some features include:

* Status message available on most screens
* Z offset, manual and automatic leveling
* User confirmation screen (used by the filament runout procedure for example)
* Power loss recovery
* Custom G-code input (requires [updating the touchscreen's core firmware](https://github.com/Desuuuu/DGUS-reloaded/wiki/Flashing-the-touchscreen-GUI-and-OS-firmware))
* PID autotuning
* Volume adjustment (saved to EEPROM)
* Brightness adjustment (saved to EEPROM)
* EEPROM reset shortcut
* BLTouch reset shortcut (if a BLTouch is installed)
* Print statistics (on the informations screen)
* Playing sounds using M300 (the frequency parameter is the index of the audio file)

Focus was also put on making this firmware as easy and safe to use as possible from a user perspective.

## Compatibility
This firmware **should** be compatible with printers equipped with the following hardware:

* 480x272 DWIN touchscreen
* Single extruder
* Heated bed
* Single controllable fan
* Bed leveling sensor (including a BLTouch)

It **could** also work on machines equipped with more hardware (dual extruder, etc.) but will lack on-screen controls for such hardware.

Testing has been done on the following machines:

* Creality CR-10S Pro
* Creality CR-10S Pro V2
* Creality Ender 5 Plus

## Prerequisites
You have to compile and flash this [modified version of Marlin](https://github.com/Desuuuu/Marlin) with `DGUS_LCD_UI_RELOADED` defined in the configuration.

Example Marlin configurations are available in [this repository](https://github.com/Desuuuu/DGUS-reloaded-config).

## Installation
The installation process is detailed on [this wiki page](https://github.com/Desuuuu/DGUS-reloaded/wiki/Flashing-the-firmware).

## Modification / Compilation
You can make modifications to the firmware by opening the `DWprj.hmi` file in **DGUS Tools**.

After finishing your modifications, you will need to press the *Generate* button to create the 3 required binary files.

You can then run the rename script and flash your touchscreen using the resulting `DWIN_SET` folder.

## Credits
| Material                                                                       | Author                                                    | Modified | License                                                               |
|:------------------------------------------------------------------------------:|:---------------------------------------------------------:|:--------:|:---------------------------------------------------------------------:|
| [Marlin logo](https://github.com/MarlinFirmware/MarlinDocumentation)           | [MarlinFirmware](https://github.com/MarlinFirmware)       | Yes      | [GPLv3](http://www.gnu.org/licenses/gpl-3.0.html)                     |
| [Feather icons](https://feathericons.com/)                                     | [Cole Bemis](https://twitter.com/colebemis)               | Yes      | [MIT](https://github.com/feathericons/feather/blob/master/LICENSE)    |
| [3D Printing Line icons](https://www.iconfinder.com/iconsets/3d-printing-line) | [Sam Baines](https://www.iconfinder.com/conceptbaines)    | Yes      | [CC-BY 3.0](https://creativecommons.org/licenses/by/3.0/legalcode)    |
| [Fan icon](https://thenounproject.com/term/fan/1153915/)                       | [Atif Arshad](https://thenounproject.com/atifarshad/)     | Yes      | [CC-BY 3.0](https://creativecommons.org/licenses/by/3.0/us/legalcode) |
| [Snow icon](https://thenounproject.com/term/snow/1959859/)                     | [Shashank Singh](https://thenounproject.com/rshashank19/) | Yes      | [CC-BY 3.0](https://creativecommons.org/licenses/by/3.0/us/legalcode) |
| [Electric Motor icon](https://thenounproject.com/term/electric-motor/2734486/) | [Verry](https://thenounproject.com/verry.dsign.creative)  | Yes      | [CC-BY 3.0](https://creativecommons.org/licenses/by/3.0/us/legalcode) |
| [Probe icon](https://thenounproject.com/term/probe/1841345/)                   | [Mohamed Mbarki](https://thenounproject.com/mb.icons)     | Yes      | [CC-BY 3.0](https://creativecommons.org/licenses/by/3.0/us/legalcode) |
| [Wheel icon](https://thenounproject.com/term/wheel/92430/)                     | [Deivid Sáenz](https://thenounproject.com/deivid.saenz)   | Yes      | [CC-BY 3.0](https://creativecommons.org/licenses/by/3.0/us/legalcode) |
| [Ruler icon](https://thenounproject.com/term/ruler/1738925/)                   | [Three Six Five](https://thenounproject.com/365)          | -        | [CC-BY 3.0](https://creativecommons.org/licenses/by/3.0/us/legalcode) |

## License
[GPLv3](http://www.gnu.org/licenses/gpl-3.0.html)
