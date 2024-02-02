# OEFW COMmunity (OEFWCOM) custom firmware for Radtel RT-890/Ruyage UV58Plus/iradio UV5118Plus
Radtel, Ruyage, iradio v1.34 (initially v1.33) transceiver firmware was originally reversed and rewritten in C by Dual Tacyhon to become Open Edition FirmWare (OEFW). Developed further by OEFW community during late 2023.

[The base source](https://github.com/OEFW-community/RT-890-custom-firmware/blob/main/README.md)

[v1.0 series bin files](https://github.com/M7OCM/890/tree/oefwc-m7ocm-archive)

[v2.0.0-v2.0.5 source](https://github.com/M7OCM/890/tree/source)

or

[v2.0.0 source](https://github.com/OEFW-community/RT-890-custom-firmware/tree/variant-olaid-v2.0.0)

Awaiting v2.0.6 pics...

v2.0.6 02022024 single binary, mic gain implementation by Xawen, few cosmetics, also I've cured (as opposed fixed) a pixel alignment "issue" which has been bugging me for months, whereby RGB coloured pixels ie RED, GREEN and BLUE "jump" by one third within their own pixel space (makes characters appear higher or lower than their actual X, Y coordinates). Credit: Xawen/OEFWCOM

![chirp-border](https://github.com/M7OCM/890/assets/128899149/2bd92a75-c296-45d2-ba77-d346ef139c0f)

The default grey border color RGB code change in Chirp (above).

![20240126_155414](https://github.com/M7OCM/890/assets/128899149/f485372a-22fe-477b-a5f6-cb7d9bb54800)

v2.0.5 27012024 (AGC Mode/Reg edit issue resolved thanks Xawen) single binary, squelch threshold revision; based on data gleaned from various UV-K5 firmware sources. Credit: Xawen/OEFWCOM

![20240126_155720](https://github.com/M7OCM/890/assets/128899149/29dbb05a-a34b-4a6f-bd0b-df814744cf50)

Note: looks identical to 2.0.4 check version Menu 74.

![20240126_090459](https://github.com/M7OCM/890/assets/128899149/13d9a187-1389-4f6c-85a9-f283eaa098ed)

![20240124_151343](https://github.com/M7OCM/890/assets/128899149/12bfc53c-a5f9-4397-820a-4724b7fa27e8)

v2.0.4 24012024 single binary, colour not mono, cosmetic, AGC Mode id in single ch/vfo. A=Auto (AM Fix) F=Fixed - manual value changes to pre existing AGC Modes. Credit: LCiccio/Reppad for dBM RSSI update

v2.0.3 21012024 two binaries mono and colour, you decide ;-) AM enhancement; full manual control or auto AM Fix, AGC modes and AM register editor. Credit: Xawen/OEFWCOM

Instructions: Assign three quick access keys via menu, I recommend Key 2, 5 and 8. All long press.

Key 2 AM Fix on/off (manual mode should be off), Key 5 AGC Mode, toggle selection and Key 8 Reg Editor.

![20240121_003114](https://github.com/M7OCM/890/assets/128899149/ae3829b8-faa2-4d7d-a67c-e25d26eb5881)

To edit registers, use up/down keys to scroll and 2/3 to decrease/increase value. Exit to save. If AM Fix is on, AUTO3 plus FIX 3, (from v2.0.4+ A3 and F3) values will be reduced automatically and then reset after squelch closes. Manual value interaction is better in my opinion as weak signal capture is vastly improved and stronger signals heard with more clarity and greater amplification. AM Fix imposes a blanket dBM reduction which leads to inconsistent audio levels. That said, it is still a viable solution for handsfree listening with no user input required.

After many weeks of testing, fixed AGC mode FIX 2 (F2) is a good starting point for excellent airband listening on a airband resonant handheld whip. Higher gain antennas (plus pre amp etc) will most likely require FIX 1 (F1). If the point of saturation is exceeded and squelch opens, the receiving frequency will reset to 000.00000. Reduce value(s) accordingly.

Users are encouraged to experiment based on location and antenna used. As a rule of thumb, high PGA combined with high LNA values will result in distortion of strong local signals. Consider reducing LNAS to value 2, and/or reducing PGA by 1 or more units.

Please note registers reset to default on shutdown.

Barring this feature and some cosmetics (status bar Dual Standby DSB changed to RX2), there is no other changes from v2.0.2 so no need to update if AM - particularly airband - isn't of interest.

"Color" version best viewed in Dark Theme as the Light Theme lacks the clarity of black on white, white on black. Thats why I dont use coloured text on a white background very often! 😉 See mono binary for that.

![20240121_002536](https://github.com/M7OCM/890/assets/128899149/f0c8c873-a1c3-46b9-87f8-6ca6e541e505)

![20240121_002405](https://github.com/M7OCM/890/assets/128899149/c939af24-118e-4c12-b5bf-89770a264862)

![20231231_224741](https://github.com/M7OCM/890/assets/128899149/396fe400-9c2d-4374-9db4-4cec73f397ad)
![20240101_030924](https://github.com/M7OCM/890/assets/128899149/6562525d-a74f-47ec-b30d-e528255266f7)

2.0.2It colour update 31122023: OEM style, blue rx etc. This a special firmware and differs cosmetically from standard. I revised this exclusively for an Italian amateur radio group on Telegram.

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
- RX 10 MHz to 1.3 GHz
- FM, AM and SSB (LSB/USB) modulation
- Light and dark theme, user selectable
- Squelch and S-meter revisions
- Full colour spectrum with options
- AM Fix (ported version @OneOfEleven's) or optional v2.0.3+ AGC mode/reg editor for enhanced AM RX
- Custom side key and quick access keys
- New configurable actions (FM Radio, Scanner, Flashlight, Dark Theme and Spectrum
- Clock speed 120 MHz (OEFWCOM 72 MHz)
- 0.01K to 5 MHz steps
- Display BK4819/ battery voltage registers in single VFO mode (firware v2.0.3+ are editable) 
- Display dBM when receiving (revised)
- Reworked scan functionality
  - 8 Scan lists
  - Faster scanning
  - Resume mode: Time, Carrier, No
  - Change scan direction while scanning (up/down keys)
  - Force scan resume (up/down keys)
- Reworked main menu
- Ability to disable LED flashing when scanning
- and many more under the hood!

![20231202_140911](https://github.com/M7OCM/890/assets/128899149/5e7548cc-7edc-402c-b838-2062303be3fe)

Usual disclaimer, experimental firmware on a radio known for spurious signals and harmonics... what could possibly go wrong?! 🧯

Use at own risk, no guarantee anything will work correctly or as intended. Back up your SPI with OEFW firmware flasher tool before using (see files).

![20231126_232206](https://github.com/M7OCM/890/assets/128899149/54afe5dd-b26f-43c8-a622-3b85a9a4fee7)

Note, the name tag font is upper case only and limited in special characters.

Chirp Next compatible only with modified python module loaded (see files).

This is a personal project for my use primarily. Its uploaded here for archiving and for others to try as is. This is my vision, it might not be yours and that is fine. Please try OEFW or the other OEFWCOM releases. The latter being fully supported by an active group on [Telegram RT890 OEFW](https://t.me/RT890_OEFW)

All versions are updated with OEFWCOM changes wherever possible making the latest release the most current or 'fixed'. That said, not all OEFWCOM features are implemented. My revisions are focussed on ui and operability for my use.

Future plans: v2.0.0 will be updated to fix bugs and add improvements to the current version. I cannot guarantee when this will happen or how long I will continue to work on this project. Its come a long way in a short space of time and is very useable now compared to stock.

OEFWCOM is an ongoing development project by enthusiasts, in their own time and for no financial gain. Testers are encouraged to provide feedback to the developers, without it, progess and implementation is unlikely to happen. So please do get involved.

[Telegram RT890 OEFW](https://t.me/RT890_OEFW)

[OEFWCOM](https://github.com/OEFW-community/RT-890-custom-firmware)

The OEFW/OEFWCOM innovators:

[Dual Tachyon](https://github.com/dualtachyon)

LCiccio

[Reppad](https://github.com/reppad)

[Superogira](https://github.com/superogira)

[Tunas1337](https://github.com/tunas1337)

[Xawen](https://github.com/xawen)

Many thanks to them all!

73

M7OCM

[Supporting Open Edition Firmware](https://ko-fi.com/dualtachyon)🔚
