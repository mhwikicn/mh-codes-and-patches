# Monster Hunter codes and patches

#### Mostly cheat codes, usable on emulators or real console with a proper cheat system.

# PS2
## Monster Hunter 2(dos) SLPM_662.80

### PSP Connection Check Bypass

Enter *CONNECT* from main menu, load your save and get ready, on *Checking MONSTER HUNTER PORTABLE* screen, press *SELECT+START* to bypass the connection check.

* Support PCSX2 mordern cheat system, can be toggled on/off
* Key combination only takes effect on checking connection screen(a total three conditional checks for actual execution), it can theoretically remain on without other effects
* Theoretically the same as connecting with a real PSP
* Tested on PCSX2(v2.0 later) and PS2 real console (OPL+PS2RD cheating system), not guaranteed for other envrionments
#### Codes for emulator
```
gametitle=Monster Hunter 2 (SLPM-66280)

[PSP Connection Check Bypass(SELECT+START)]
author=PoogieCharger
description=Press SELECT+START to bypass Monster Hunter Portable connection check.
patch=1,EE,E0040002,extended,00AC8158
patch=1,EE,E003000B,extended,00AC8154
patch=1,EE,E002FFF6,extended,0024BC1C
patch=1,EE,10AC95C0,extended,00000FFF
patch=1,EE,70AC8100,extended,00000001
```
#### Codes file for emulator(.pnach)
[Download](./SLPM-66280_2F0E94A1_PSP_Connection_Check_Bypass.pnach)
#### Raw codes
```
E0040002 00AC8158
E003000B 00AC8154
E002FFF6 0024BC1C
10AC95C0 00000FFF
70AC8100 00000001
```

Last update: 2025/11/09 by PoogieCharger
