# Monster Hunter codes and patches

#### Mostly cheat codes, for emulators or real hardware system with a proper cheat support.

# PS2
## Monster Hunter 2(dos) SLPM_662.80

### PSP Connection Check Bypass

Enter *CONNECT* from main menu, load your save and get ready, on *Checking MONSTER HUNTER PORTABLE* screen, press *SELECT+START* to bypass the connection check.

* Support PCSX2 mordern cheat system, can be toggled on/off
* Key combination only takes effect on checking connection screen(a total three conditional checks for actual execution), it can theoretically remain on without other effects
* Theoretically the same as connecting with a real PSP
* Tested on PCSX2(v2.0 later) and PS2 fat 30000 model (OPL+PS2RD), not guaranteed for other envrionments
#### Codes for emulator
```
gametitle=Monster Hunter 2 (SLPM-66280)

[PSP Connection Check Bypass(SELECT+START)]
author=PoogieCharger
description=Press SELECT+START to bypass connection check with Monster Hunter Portable.
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
# PSP
## Monster Hunter Portable(MHP) ULJM-05066

### PS2 Connection Check Bypass

Enter *CONNECT* from main menu, load your save and get ready, on *Checking MONSTER HUNTER 2* screen, press *SELECT+START* to bypass the connection check.

* Cannot prevent repeated triggering(for now), please don't press the key combination outside the CONNECT screen, or just disable the codes when not in use
* Theoretically the same as connecting with a real PS2
* Tested on PPSSPP(v1.19.3) and PSP 3000 model(Ark-4 cfw+Cheat Master Fusion), not guaranteed for other envrionments
#### Codes for emulator
```
_C1 PS2 Connection Check Bypass(SELECT+START)
Press SELECT+START to bypass connection check with Monster Hunter 2.
_L 0xE0030009 0x00179e94
_L 0xE0020001 0x00224848
_L 0x102248C0 0x000039FF
_L 0x00224848 0x00000003

```
#### Codes file for emulator(.ini)
[Download](./ULJM05066_PS2_Connection_Check_Bypass.ini)


###### Last update: 2025/11/09 by PoogieCharger
