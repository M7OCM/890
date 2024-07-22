# Modified OEFWCOM Transceiver Firmware for Radtel RT-890

**890-I PCB 2.0 Only**

For new PCB 2.1 model firmware/source files see [here](https://github.com/M7OCM/890-II)

[Source files v2.0.0+](https://github.com/M7OCM/890/tree/source)

[Compiled bin files](https://github.com/M7OCM/890/tree/binary)

**LATEST**

M7OCM v2.1.8 PCB 2.0 Firmware based on Open Edition Firmware Community [OEFWCOM](https://github.com/OEFW-community/RT-890-custom-firmware)

![20240712_155609](https://github.com/user-attachments/assets/b605e3be-6fbc-42fb-bfd8-c8cc5422fbef)

PCB 2.0 only - don't use the PCB 2.1 version! All bin files are now in the binary branch.

AM enhancements, UI changes, channel digits moved to more appropriate location, scan resume times adjusted: carrier 5.5s/time 2.5s. Scan speed reduced to stock as everything works correctly that way. It can be increased by adjusting the countdown times in the firmware (see source files). The 2.0 PCB firmware differs from the 2.1 PCB firmware (and I expect more changes to 2.1 independant of this model firmware). With that in mind there is no makefile compile option to switch between hardware versions. Of course anyone can change this should they wish.

This is a personal project for my use primarily. Unfortunately, I cannot accomodate feature requests due to time constraints - this is just a hobby I do for fun (joke). Its "as is". If you don't like it, or it doesn't perform to your expectations don't use it or join forces - fork your own version, modify mine or start from scratch; code freely available via the links below.

[OEFWCOM](https://github.com/OEFW-community/RT-890-custom-firmware)

[DualTachyon OEFW UV-K5/RT-890](https://github.com/dualtachyon)

**Default Keys**

- Side Key [1SP] Monitor
- Side Key [1LP] Freq Detect
- Side Key [2SP] Scan/Advance Scan List/Scan Stop (LP)
- Side Key [2LP] Spectrum

SP = Short Press; LP = Long Press

The following keypad keys are all LP

- [1] Squelch
- [2] Modulation
- [3] Bandwidth
- [4] TX Power
- [5] AM Fix
- [6] Dual Standby
- [7] Repeater Mode
- [8] Reg Editor
- [9] Scan List Add or remove a channel to current scan list
- [0] FMB
- [*] Edit TX Freq
- [#] Lock
- [MENU] TX CTCSS/DCS
- [EXIT] Single/Dual Display

**Spectrum**

Enter by pressing side key 2 LP

- [Up] Increase frequency range
- [Down] Decrease frequency range
- [1] Change scan step (16, 32, 64 or 128)
- [3] Change modulation FM, AM or SB (SSB)
- [4] Change step size (0.25k - 50k)
- [5] Switch spectrum modes (toggle 1-4)
- [6] Increase squelch level
- [7] Hold/Search (in hold, use up/down to adjust main frequency - useful to avoid RFI)
- [9] Decrease squelch level
- [0] Toggle filter (X = unfiltered, F = filtered)
- [*] Change scan delay (0 - 10ms)
- [#] Toggle bandwidth (25.0K = wide, 12.5K = narrow)
- [MENU] Jump to VFO mode with current frequency and settings (to allow TX)
- [EXIT] Return to main

SP [#] switch between VFO-CH mode

**Register Editor**

Press key 8 LP and Register Editor will launch, showing the current register values. The register currently being edited will display in large font.

- [Up] Move editor to next register
- [Down] Move to previous register
- [1] Change RF Gain Control (AGC 3, FGC 3/2/1/0/7/6/5/4); FGC 2 is a good choice for airband. If AM Fix is on, use AGC 3 (default). Turn AM Fix off if using FGC
- [2] Decrease value of current register's setting by 1
- [3] Increase value of current register's setting by 1
- [EXIT] Return to main

AGC = Auto Gain Control. FGC = Fixed Gain Control.

FGC is a manual option - user selects parameters for fine tuning AM signals to prevent front end overloading.

- LNAS Coarse attenuator (short)
- LNA Fine tuning attenuator
- PGA Programmable threshold amplifier
- MIX Mixer gain
- BW Bandwidth filter 
- WK Weak signal threshold

**Scan lists and Scanning**

There are 8 scan lists plus scan all. Active lists are displayed in the status bar when scanning.

The current channel can be added to any scanlist using the Ch In List # menus.

The scanlist to be used can be selected in the List To Scan menu.

To ignore scanlists and scan all channels, select Scan All in the List To Scan menu.

To add/remove current channel to/from current scanlist, use the Toggle SList shortcut which is Key 9.

To start scanning, press a key mapped to the Freq scanner shortcut (default: short press side key 2).

When scanning is in progress, use side key 2 (short press) to change the scan list. This action will move to the next non-empty scanlist, or switch to scan all mode if all subsequent lists are empty.

To change the direction of current scan, use the up/down keys.

To force the scan to resume when the scanner stops on a signal, use the up/down keys.

Press any key other than Freq scanner to stop scanning.

Alternatively use Chirp Next to store scan list memory.

**Chirp Next**

Chirp Next instructions: Open in Developer mode, restart, load module (a modified Python driver), select View "Show extra fields" to display scan lists. There needs to be at least 2 frequencies per scan list but no max limit. Duplicate frequencies can be added to more than one list. Try the example .img file which contains 16 PMR446 frequencies in Scan List 1. Download/upload to radio use Vendor: Ruyage, Model: UV58Plus

The Chirp driver is a WIP. 8.333kHz channels can be entered and saved as can any frequency in the range 10MHz to 1.3GHz. All modulation modes. Scan Lists can be modified. Border colour can be changed and basic radio functions adjusted. Not all key actions save however. A key reset Menu #67 after upload fixes that. I reccomend making copies of data files on a regular basis just in case a file becomes corrupted which may happen when switching between different firmware versions (latest always works).

Note. When entering a 8.333kHz frequency in Chirp, this needs to be entered in its entirety eg 118.00833 (note the 5 decimal places). Attempting to enter or copy/paste from a CSV file something like 133.91667 or 133.91670 will not work. Enter the full correct step size ie 133.91666.

**FM Broadcast (FMB)**

Default [0/FM], toggle FMB On/FMB Idle. The 4 digit FM frequency now appears in the upper left part of the status bar. It works the same as stock just without the garbage graphics. Turn on FM Standby via menu, and you can listen to FMB while scanning/searching. When a signal is present the FM radio will mute, then continue until another signal appears - pretty cool! Note using the FMB after Spectrum may result in poor reception, no reception or work as normal, this is generally linked to specfic bands such as 440 MHz (probably many more). Open squelch to reset chip registers usually works, reboot, or select scan then FMB. This is a known issue. The radio uses a dedicated FMB chip not the BK4819. Resetting the latter clears any issues though.

To clear the idle frequency, press [0/FM] or [PTT] then [MENU].

**Status Bar**

(l-r) Padlock = Lock, FMB, V = VOX, Scan List #, D = Dual Standby/S = Single RX, Repeater Mode "-" = No RX Subtone, "=" = Monitor Input, TX Tone A = Roger Beep A, B = Roger Beep B, I = Send FSK ID, Battery Icon = Cell charge status.

The default border color used is grey (33808). The code change can be made in Chirp or Radtel's CPS software. Please note if using the latter to change logo or border colour, CPS will throw an error after reading from radio. Nothing else gets changed during upload, but best save a Chirp back up file before proceeding. Always download to radio first, don't change border colour and upload as the data will/could get corrupted and/or overwritten (backup data regularly just in case).

**Speech Inversion Frequencies**

- 1 1350Hz
- 2 1400Hz
- 3 1450Hz
- 4 1500Hz
- 5 1550Hz
- 6 1600Hz
- 7 1650Hz
- 8 1700Hz

## Features in v2.1.8 PCB 2.0

- RX is unlocked 10 MHz to 1.3 GHz CAUTION experimental use only. BK4819 (useable) RX is approx 50-600 MHz; Reception outside of this range is possible but not guaranteed; radio may also exhibit erratic behaviour.

- TX 2m/70cm officially, plus various VHF/UHF bands 136-470 MHz. Output varies by band: 2-6W generally on High; max 3.6W on Low power - all figures approx - your mileage may vary 💀 CAUTION do not TX outside of chip specification, it could destroy your radio and/or breach your country of residence radio communications laws/license agreement 💀

- 0.01K to 5 MHz steps
- 999 channel memory
- (N/W)FM, (N/W)AM and SSB (SB) (LSB/USB) modulation
- Light and dark theme, user selectable
- Restyled ui, fixed alignment issues, renamed menu items, new use for status bar (Scan List #), colour changes, font changes, improved clarity etc
- Squelch sensitivty and S-meter revisions
- DCS RX revised/Freq Detect DCS fixed
- PTT BCLO TX during monitor revised, PTT now TX when monitor is open
- RSSI timer speed reduction to reduce internal RFI caused by SPI (screen) updates
- Full colour spectrum with control options, views
- AM Fix ported from 1 of 11's UV-K5 firmware (modified by me)
- RF Gain Control and Register Editor
- Flashlight Mode
- NOAA Monitor
- Custom side key and configurable "quick access" keypad keys
- Clock speed 120 MHz (stock 72 MHz)
- Display BK4819 AGC Modes/battery voltage registers in single VFO mode
- Display dBM when receiving (calculation accuracy revised)
- Reworked scan functionality
 - 8 Scan lists plus scan all
 - Scan is stock otherwise it breaks things
 - Resume mode: Time/TO (5.5s), Carrier/CO (2.5s), No resume/SE
 - Change scan direction while scanning (up/down keys)
 - Force scan resume (up/down keys)
- Reworked main-sub menu system, renamed items
- ... bear in mind not all OEFWCOM features are included and some of mine are unique!

Important note, the 10 character name tag font is UPPER CASE English alphanumeric only and limited in special characters/punctuation: . : - = < > @ ?

Please note the files herein are two colour themes (light/dark) only, not multiple colour versions that can be switched within the radio menu.

**Disclaimer, experimental firmware on a radio known for spurious signals and harmonics... what could possibly go wrong?!** 🧯

**Use at own risk, no guarantee anything will work correctly or as intended. Back up your SPI with OEFW firmware flasher tool before using (see files) and radio data with Chirp Next.**

## OEFWCOM

OEFWCOM is an ongoing development project by enthusiasts, in their own time and for no financial gain. Testers are encouraged to provide feedback to the developers, without it, progess and implementation is unlikely to happen. So please do get involved.

[Telegram RT890 OEFW](https://t.me/RT890_OEFW)

[OEFWCOM](https://github.com/OEFW-community/RT-890-custom-firmware)

## OEFW/OEFWCOM

[DualTachyon](https://github.com/dualtachyon)

[CR7BLE](https://github.com/jcalado)

LCiccio

Marcos

[Psy97x](https://github.com/Psy97x)

[Reppad](https://github.com/Reppad)

[Superogira](https://github.com/superogira)

[Tunas1337](https://github.com/tunas1337)

[Xawen](https://github.com/xawen)

Many thanks to them all!

73

M7OCM

[Supporting Open Edition Firmware](https://ko-fi.com/dualtachyon)🔚
