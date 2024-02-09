# OEFW COMmunity (OEFWCOM) custom firmware for Radtel RT-890/Ruyage UV58Plus/iradio UV5118Plus
![20240209_105633](https://github.com/M7OCM/890/assets/128899149/0d65071a-431f-4832-acfc-9845ab84e00f)

## Latest
v2.0.8-naf coming soon... this will be the last firmware update from me. If you prefer AM Fix use standard v2.0.7.

Personal thanks to Reppad and Xawen for assisting me in this project 👍

v2.0.7-naf 07022024 for HARDCORE AIRBAND users 😂 NO AM FIX, yes you read that correctly! I have removed all of 1of11s ported code, so AM reception is in your hands via the AGC Mode/Reg Editor!!! Use PGA wisely haha overload at your peril!

Key 2 preset (was AM Fix) is defaulted to Flashlight mode for time being (is already changed in upcoming v2.0.8-naf, to original TX Priority). The 2.0.7-naf menu AM Fix option is replaced by *AM Fix Void - if selected, this again defaults to Flashlight, just as a reminder this is a no AM Fix firmware edition 😉

AGC Mode and Reg Editor; same setup and keys, however for airband it is advised to use AGC Mode F2 (or F1 if using an external antenna) or change values to suit your antenna, location etc. Unless using a nail as an antenna 😁 AGC Modes A3 and F3 provide too much gain without AM Fix. These values are OEM default for FM RX. Hence the overloading issue with AM on stock. Try it though maybe be useable to some.

VHF airband tips. Using a commonly available 771 type antenna, good location for air traffic, set F2. Test for local overloading and try reducing LNAS3 to 2. If reception is borderline try LNA 4 and PGA 3 or 4. I have mine on default F2 (all the 3's barring BW4 WK0). Sometimes for military UHF airband, I'll bump up LNA and PGA to 4. LNAS can be adjusted accordingly. Best to experiment not only with registers but antennae. Stock works well on airband despite the bad rep it receives online.

FM can be greatly enhanced. Crank up the gain it works wonders. Try it!

As before, registers reset when unit is switched off, but remain active while powered on. AGC Mode works in vfo, channel and spectrum modes.

v2.0.7 07022024 a minor revision, includes CR7BLE's excellent RSSI timer update (slows down screen updates to reduce interference). Credit: OEFWCOM

Experimental ui I've been working on! Bringing back the gawd awful display divider lines 😁 That required a major overhaul of individual display coordinates and really shows up a wonky screen of which I have 2! Looks better than stock I think pretty crammed in though. Playing with S-bar styles too. Back burner projects those. Some bits might get used.

![20240206_075833](https://github.com/M7OCM/890/assets/128899149/86dea561-664c-4a53-8526-8f1dc07290f7)

![20240204_231208](https://github.com/M7OCM/890/assets/128899149/a0bfbfc2-b8df-4158-975c-06fb8a464de7)

![20240204_152010](https://github.com/M7OCM/890/assets/128899149/33220955-c419-41e2-8304-e6dd5704d353)

## Background and previous versions
Radtel, Ruyage, iradio v1.34 (initially v1.33) transceiver firmware was originally reversed and rewritten in C by Dual Tacyhon to become Open Edition FirmWare (OEFW). Developed further by OEFW community during late 2023.

[The base source](https://github.com/OEFW-community/RT-890-custom-firmware/blob/main/README.md)

[v1.0 series bin files](https://github.com/M7OCM/890/tree/oefwc-m7ocm-archive)

[v2.0.0-v2.0.6 source](https://github.com/M7OCM/890/tree/source)

or

[v2.0.0 source](https://github.com/OEFW-community/RT-890-custom-firmware/tree/variant-olaid-v2.0.0)

![20240202_163643](https://github.com/M7OCM/890/assets/128899149/d6de065f-08c9-4761-a4b2-8702bca57a0c)

![20240202_155859](https://github.com/M7OCM/890/assets/128899149/922f0b51-a662-49a3-a350-97c8e1f3bc92)

v2.0.6 02022024 single binary, mic gain implementation by Xawen, few cosmetics, also I've cured (as opposed fixed) a pixel shift "issue" which has been bugging me for months, whereby coloured pixels notably RED and BLUE "move" within their own pixel space, making characters appear higher or lower than their actual X, Y code coordinates. Credit: Xawen/OEFWCOM

![chirp-border](https://github.com/M7OCM/890/assets/128899149/2bd92a75-c296-45d2-ba77-d346ef139c0f)

The default border color used in v2.0.6 is grey. The code change can be made in Chirp (see above) or Radtel's CPS software. Please note if using the latter to change logo or border colour, CPS will throw an error after reading from radio. Nothing else gets changed during upload, but best save a Chirp back up file before proceeding. Always download to radio first, don't change border colour and upload as the data will/could get corrupted (backup data regularly just in case).

![20240126_155414](https://github.com/M7OCM/890/assets/128899149/f485372a-22fe-477b-a5f6-cb7d9bb54800)

v2.0.5 27012024 (AGC Mode/Reg edit issue resolved thanks Xawen) single binary, squelch threshold revision; based on data gleaned from various UV-K5 firmware sources. Credit: Xawen/OEFWCOM

![20240126_155720](https://github.com/M7OCM/890/assets/128899149/29dbb05a-a34b-4a6f-bd0b-df814744cf50)

Note: looks identical to 2.0.4 check version Menu 74.

![20240126_090459](https://github.com/M7OCM/890/assets/128899149/13d9a187-1389-4f6c-85a9-f283eaa098ed)

![20240124_151343](https://github.com/M7OCM/890/assets/128899149/12bfc53c-a5f9-4397-820a-4724b7fa27e8)

v2.0.4 24012024 single binary, colour not mono, cosmetic, AGC Mode id in single ch/vfo. A=Auto (AM Fix) F=Fixed - manual value changes to pre existing AGC Modes. Credit: LCiccio/Reppad for dBM RSSI update

v2.0.3 21012024 two binaries mono and colour, you decide ;-) AM enhancement; full manual control or auto AM Fix, AGC modes and AM/FM register editor. Credit: Xawen/OEFWCOM

Instructions: Assign three quick access keys via menu, I recommend Key 2, 5 and 8. All long press.

Key 2 AM Fix on/off (manual mode should be off), Key 5 AGC Mode, toggle selection and Key 8 Reg Editor.

![20240121_003114](https://github.com/M7OCM/890/assets/128899149/ae3829b8-faa2-4d7d-a67c-e25d26eb5881)

To edit registers, use up/down keys to scroll and 2/3 to decrease/increase value. Exit to save. If AM Fix is on, AUTO3 plus FIX 3, (from v2.0.4+ A3 and F3) values will be reduced automatically (when necessary) to prevent overloading and then reset to default after squelch closes.

Manual value interaction is better in my opinion as weak signal capture is vastly improved and stronger signals heard with more clarity and greater amplification. AM Fix tends to impose a blanket dBM reduction leading to inconsistent audio levels. That said, it is still a viable solution for handsfree listening with no user input required.

After many weeks of testing, fixed AGC mode FIX 2 (F2) is a good starting point for excellent airband listening on a airband resonant handheld whip. Higher gain antennas (plus pre amp, external roof mounted etc) will likely require FIX 1 (F1). If the point of saturation is exceeded and squelch opens, the receiving frequency will reset to 000.00000. Reduce value(s) accordingly.

Users are encouraged to experiment based on location and antenna used. As a rule of thumb, high PGA combined with high LNA values will result in distortion of strong local AM signals. Consider reducing LNAS to value 2, and/or reducing PGA by 1 or more units.

Please note registers reset to default on shutdown. All BK4819 AGC modes are available though F0, F7, F6 and F5 are undocumented and most have default zero values, some of those values are unchangeable which is normal behaviour. Unlike AM fix, register edits also work on FM.

Barring this feature and some cosmetics (status bar Dual Standby DSB changed to RX2), there is no other changes from v2.0.2 so no need to update if AM - particularly airband - isn't of interest.

"Color" version best viewed in Dark Theme as the Light Theme lacks the clarity of black on white, white on black. Thats why I never used coloured text on a white background! 😉 See mono binary for that.

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
- (N/W)FM, (N/W)AM and SSB (LSB/USB) modulation
- Light and dark theme, user selectable
- Squelch and S-meter revisions
- Full colour spectrum with options
- AM Fix (ported version of OneOfEleven's) or optional v2.0.3+ AGC mode/reg editor for enhanced AM RX; AM Fix removed in v2.0.7-naf, v2.0.8-naf
- Custom side key and quick access keys
- New configurable actions (FM Radio, Scanner, Flashlight, Dark Theme and Spectrum
- Clock speed 120 MHz (OEFWCOM 72 MHz)
- 0.01K to 5 MHz steps
- Display BK4819/ battery voltage registers in single VFO mode (firmware v2.0.3+ reg are editable) 
- Display dBM when receiving (revised)
- Reworked scan functionality
  - 8 Scan lists
  - Faster scanning (16 ch/s)
  - Resume mode: Time, Carrier, No resume
  - Change scan direction while scanning (up/down keys)
  - Force scan resume (up/down keys)
- Reworked main menu
- Ability to disable LED flashing when scanning
- and many more improvements...

![20231202_140911](https://github.com/M7OCM/890/assets/128899149/5e7548cc-7edc-402c-b838-2062303be3fe)

Usual disclaimer, experimental firmware on a radio known for spurious signals and harmonics... what could possibly go wrong?! 🧯

Use at own risk, no guarantee anything will work correctly or as intended. Back up your SPI with OEFW firmware flasher tool before using (see files) and radio data with Chirp.

![20231126_232206](https://github.com/M7OCM/890/assets/128899149/54afe5dd-b26f-43c8-a622-3b85a9a4fee7)

Note, the name tag font is upper case only and limited in special characters.

Chirp Next compatible only with modified python module loaded (see files).

## OEFWCOM and my plans

This is a personal project for my use primarily. Its uploaded here for archiving and for others to try as is. This is my vision, it might not be yours and that is fine. Please try OEFW or the other OEFWCOM releases. The latter being fully supported by an active group on [Telegram RT890 OEFW](https://t.me/RT890_OEFW)

All versions are updated with OEFWCOM changes wherever possible making the latest release the most current and/or 'fixed'. That said, not all OEFWCOM features are implemented. My revisions are focussed on ui and operability for my use.

Future plans: v2.0.0 will be updated to fix bugs and add improvements to the current version. I cannot guarantee when this will happen or how long I will continue to work on this project. OEFW 890 has come a long way in a very short space of time and is very useable now compared to stock.

OEFWCOM is an ongoing development project by enthusiasts, in their own time and for no financial gain. Testers are encouraged to provide feedback to the developers, without it, progess and implementation is unlikely to happen. So please do get involved.

[Telegram RT890 OEFW](https://t.me/RT890_OEFW)

[OEFWCOM](https://github.com/OEFW-community/RT-890-custom-firmware)

## Team OEFW/OEFWCOM

[DualTachyon](https://github.com/dualtachyon)

[CR7BLE](https://github.com/jcalado/RT-890-custom-firmware/commit/eb97ae261845ca510c69076e9ddd0735dda79b8d)

LCiccio

[Superogira](https://github.com/superogira)

[Tunas1337](https://github.com/tunas1337)

[Xawen](https://github.com/xawen)

Many thanks to them all!

73

M7OCM

[Supporting Open Edition Firmware](https://ko-fi.com/dualtachyon)🔚
