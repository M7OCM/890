# OEFW Community (OEFWCOM) custom firmware for Radtel RT-890/Ruyage UV58Plus/iradio UV5118Plus
[The base source](https://github.com/OEFW-community/RT-890-custom-firmware/blob/main/README.md)

[2.00-2.02 source](https://github.com/M7OCM/890/tree/source)

or

[2.0.0 source](https://github.com/OEFW-community/RT-890-custom-firmware/tree/variant-olaid-v2.0.0)

Radtel, Ruyage, iradio v1.34 firmware, originally reversed and rewritten by Dual Tacyhon to become OEFW. Developed further by OEFWCOM during late 2023.

![20231231_224741](https://github.com/M7OCM/890/assets/128899149/396fe400-9c2d-4374-9db4-4cec73f397ad)
![20240101_030924](https://github.com/M7OCM/890/assets/128899149/6562525d-a74f-47ec-b30d-e528255266f7)

2.0.2It colour update 31122023: OEM style, blue rx etc. This a special firmware and differs cosmetically from standard. I designed this exclusively for an Italian group on Telegram.

2.0.2 refactoring 21122023 one bin: black/white (default). Credit: OEFWCOM

2.0.1 bug fixes 18122023 two bins: black/green; black/orange. Credit: OEFW - OEFWCOM

2.0.0 official release 13122023 two bins: black/green; black/orange. Credit: OEFW - OEFWCOM

![20231213_164050](https://github.com/M7OCM/890/assets/128899149/74cf0357-34b5-433f-a620-4f2a853c2a49)

![20231213_164032](https://github.com/M7OCM/890/assets/128899149/72efdbd4-1906-4ca0-bf35-fc0a35ed616d)

![20231211_115816](https://github.com/M7OCM/890/assets/128899149/a705ff8e-1d42-4629-961f-bc3d377b8329)

![20231218_080633](https://github.com/M7OCM/890/assets/128899149/626091d6-d302-4776-957c-7a9b31841fca)

![20231207_215408](https://github.com/M7OCM/890/assets/128899149/a0231b84-7295-4c95-a65f-3602a05e64b9)

Please note the bin files herein are 2 colour themes only, not multiple colour versions that can be switched within the radio menu. Schemes can be readily changed in ui/gfx.c (info in file).

![20231207_082721](https://github.com/M7OCM/890/assets/128899149/8b22bb4d-8f40-4794-a051-b7f379ca8464)

![20231207_215538](https://github.com/M7OCM/890/assets/128899149/a35c4a4f-4139-4193-b0d9-284de1c573d4)

Spectrum. Key 5 to switch spectrum colours/display variations.

Scanning speed improvements equate to around 16 ch/s or about 999 ch/m - not too shabby considering how slow stock is.

## Features
- All stock features: [check user's manual](https://cdn.shopifycdn.net/s/files/1/0564/8855/8800/files/RT-890_user_manual.pdf?v=1670288968)
- RX frequency can be set from 10 to 1300 MHz (results may vary)
- LSB/USB reception
- Light theme
- Full colour spectrum with user options
- AM Fix (improvement in AM reception with strong signals, port of @OneOfEleven's excellent work on the Quansheng UV-K5)
- Full control over side key and main key shortcuts
- New configurable actions (FM Radio, Scanner, FLashlight, Dark Theme, Spectrum)
- 0.01K to 5 MHz steps
- Display registers in single VFO mode
- Display dBM when receiving
- Reworked scan functionality
  - 8 Scan lists
  - Faster scanning
  - Resume mode: Time, Carrier, No
  - Change scan direction while scanning (up/down keys)
  - Force scan resume (up/down keys)
- Reworked main menu
- Ability to disable LED flashing when scanning
- And much more!

![20231202_140911](https://github.com/M7OCM/890/assets/128899149/5e7548cc-7edc-402c-b838-2062303be3fe)

[v1.0-v2.0.1 bin files](https://github.com/M7OCM/890/tree/oefwc-m7ocm-archive)

Usual disclaimer, experimental firmware on a radio known for spurious signals and harmonics... what could possibly go wrong?! 🧯

Use at own risk, no guarantee anything will work correctly or as intended. Back up your SPI with OEFW Flasher tool before using (see files).

![20231126_232206](https://github.com/M7OCM/890/assets/128899149/54afe5dd-b26f-43c8-a622-3b85a9a4fee7)

Note, the name tag font is upper case only and limited in special characters.

Chirp Next compatible only with Reppad's python module loaded (see files).

This is a personal project for my use primarily. Its uploaded here for archiving and for others to try as is, no feedback requested. This is my vision, it might not be yours and that is fine. Please try OEFW or the other OEFWCOM releases. The latter being fully supported by an active group on [Telegram RT890 OEFW](https://t.me/RT890_OEFW)

All versions are updated with OEFW/OEFWCOM fixes wherever possible making the latest release the most current or 'fixed'. That said, not all OEFWCOM features are implemented (ie no spectrum band presets or waterfall). My revisions are focussed on ui and operability for my use.

Plan. v2.0.0 will (for the time being) only be updated to fix bugs/improvements to the current version. I see this project as, on the whole, a finshed demonstration of a much improved firmware, containing the best features (IMO), currently developed to date of release.

The firmware is community based and written by numerous developers. For a full feature list please visit OEFWCOM.

OEFWCOM projects that are in development include s-meter and squelch threshold revisions plus enhanced AM register correction to further improve that area. All of this is being done by enthusiasts, in their own time and for no financial gain. Testers are encouraged to provide feedback to the developers, without it, progess and implementation is unlikely to happen. So please get involved.

[Telegram RT890 OEFW](https://t.me/RT890_OEFW)

[OEFWCOM](https://github.com/OEFW-community/RT-890-custom-firmware)

The OEFW/OEFWCOM innovators:

[Dual Tachyon](https://github.com/dualtachyon)

[Reppad](https://github.com/reppad)

[Superogira](https://github.com/superogira)

[Tunas1337](https://github.com/tunas1337)

[Xawen](https://github.com/xawen)

Many thanks to them all!

73

M7OCM

[Supporting Open Edition Firmware](https://ko-fi.com/dualtachyon)🔚
