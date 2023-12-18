# OEFW Community (OEFWCOM) custom firmware for Radtel RT-890/Ruyage UV58Plus/iradio UV5118Plus
[The base source] (https://github.com/OEFW-community/RT-890-custom-firmware/blob/main/README.md)

iradio v1.34 firmware reversed by Dual Tacyhon to become OEFW and developed further by OEFWCOM during late 2023.

2.0.1 bug fixes 18122023 two bins: black/green; black/orange. Fixes credit: Dual Tachyon, Xawen and Reppad.

2.0.0 Official release 13122023 two bins: black/green; black/orange.

![20231213_164050](https://github.com/M7OCM/890/assets/128899149/74cf0357-34b5-433f-a620-4f2a853c2a49)

![20231213_164032](https://github.com/M7OCM/890/assets/128899149/72efdbd4-1906-4ca0-bf35-fc0a35ed616d)

![20231211_115816](https://github.com/M7OCM/890/assets/128899149/a705ff8e-1d42-4629-961f-bc3d377b8329)

v1.9 status bar updated, removed DW, VOX icons, updated RR/TR text. DSB = Dual StandBy; VOX = VOX, RPT = RR/=, TLK = TR/-

![20231209_171937](https://github.com/M7OCM/890/assets/128899149/91e02a14-3d95-4595-a1ed-f3dcedff893d)

v1.8.5 two high contrast themes (black/orange and black/green), spectrum cosmetics.

![20231207_215408](https://github.com/M7OCM/890/assets/128899149/a0231b84-7295-4c95-a65f-3602a05e64b9)

v1.8 (+1.8.5, 1.9 & 2.0.0) released 07122023 featuring Superogira's fantastic colour mods for the Spectrum. Key #5 to switch color modes.

Open monitor after using spectrum to reset registers before using FM broadcast radio (FMB can stall at times).

Please note the bin files herein are 2 colour themes only, not multiple colour versions that can be switched within the radio menu. Schemes can be readily changed in ui/gfx.c (info in file).

![20231207_082721](https://github.com/M7OCM/890/assets/128899149/8b22bb4d-8f40-4794-a051-b7f379ca8464)

![20231207_215538](https://github.com/M7OCM/890/assets/128899149/a35c4a4f-4139-4193-b0d9-284de1c573d4)

![20231202_141014](https://github.com/M7OCM/890/assets/128899149/1406cd9d-eb8a-4bb2-b483-9571b9a5df4e)

[v1.0+ bin files](https://github.com/M7OCM/890/tree/oefwc-m7ocm-archive)

💀 Usual disclaimer, experimental firmware on a radio known for spurious signals and harmonics... what could possibly go wrong?! 🧯

Use at own risk, no guarantee anything will work correctly or as intended. Provided as is for ham operators to evaluate ☠ Goes without saying back up your SPI with OEFW Flasher tool.

![20231126_232206](https://github.com/M7OCM/890/assets/128899149/54afe5dd-b26f-43c8-a622-3b85a9a4fee7)

Note, the name tag font is upper case only and limited in special characters.

Chirp Next compatible only with Reppads python module loaded (see code files). This enables AM, FM, LSB and USB and scan lists to be saved plus proper 8.33kHz channels (no 8.33kHz step). Note, the border color is hardcoded so won't change if fettled with in Chirp.

This project started as a personal project - I'm not a developer more a radio user, but have experience with ui design and development on small oled screens. I decided to concentrate on light and dark contrast themes rather than continue with stock. Acceptable legibility at most light levels in light theme mode.

All versions are updated with OEFWCOM changes but not all are implemented (ie no spectrum band presets; includes cosmetic and layout differences). You'll either like it or not 😂 such as the experimental placement of FM broadcast frequency/play in status bar.

v2.0.0 will only be updated to fix bugs/original issues. I see this project as a finshed example of a much improved firmware containing the best features (IMO), currently developed to date of release. I hope to start working on a totally new 890 design in 2024.

The firmware is community based and features numerous improvements: an enhanced menu, frequency band/modulation expansion, 1of11's 'AM Fix' ported/modded for 890, scan resume, preset channels, 8 scan lists and full colour spectrum to name a few.

https://github.com/OEFW-community/RT-890-custom-firmware

The OEFW/OEFWCOM innovators:

Dual Tachyon "The Boss" OEFW reverse engineer, Andrej (Tunas1337) 890 modder extraordinaire, plus Reppad (legend helper) and Xawen adding an unbelievably innovative menu using free flash space and features galore like scan lists and spectrum. Special mention to Superogira for the amazing colour spectrum mods.

Many thanks to them all!

73

M7OCM

[Supporting Open Edition Firmware]
(https://ko-fi.com/dualtachyon)
🔚
