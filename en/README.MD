# Monster Hunter code and patches

#### Mostly cheat code, for emulators or real hardware system with a proper cheat support.

# PS2

## RangedWeaponCameraLock
In the original game, when aiming with a ranged weapon and then canceling the aim (bowgun: release L1, bow: release R1), the camera height automatically adjusts based on the aiming view. This code allows you to lock the camera height so it is not affected by ranged weapon aiming.
* Press START + → to enable the function, press START + ← to disable and revert to the original behavior.

### Monster Hunter 2(dos) SLPM_662.80
#### Code for emulator
```
gametitle=Monster Hunter 2 (SLPM-66280)

[RangedWeaponCameraLock]
author=PoogieCharger
description=When returning to the normal view after aiming with a ranged weapon (bowgun: release L1, bow: release R1), the camera height from before aiming is maintained. Press START + → to enable, START + ← to disable.
patch=1,EE,D024BC1C,extended,0300FFD7
patch=1,EE,D031B1B0,extended,02000070
patch=1,EE,D031B1B2,extended,0100A264
patch=1,EE,2031B1B0,extended,00000000
patch=1,EE,D024BC1C,extended,0300FF77
patch=1,EE,D031B1B0,extended,02000000
patch=1,EE,D031B1B2,extended,01000000
patch=1,EE,2031B1B0,extended,A2640070
```
#### Code file for emulator(.pnach)
[Download](./SLPM-66280_2F0E94A1_RangedWeaponCameraLock.pnach)
#### Raw code
```
E003FFD7 0024BC1C
E0020070 0031B1B0
E001A264 0031B1B2
2031B1B0 00000000
E003FF77 0024BC1C
E0020000 0031B1B0
E0010000 0031B1B2
2031B1B0 A2640070
```

## TeamLeaderPopupKiller
In MH2 online mode, a popup window saying 'The team leader is...' may sometimes appear, preventing normal gameplay. In situations where multiplayer PvP cannot proceed properly, you can press L2+L3 to close the popup window. In theory, this should have no other side effects.
* If the server supports multiplayer PvP in the future and this popup window is no longer an issue, please consider disabling the code or avoid pressing the key combination, and only press it when an abnormal popup window appears.

### Monster Hunter 2(dos) SLPM_662.80
#### Code for emulator
```
gametitle=Monster Hunter 2 (SLPM-66280)

[TeamLeaderPopupKiller(L2+L3)]
author=PoogieCharger
description=when you get a "the team leader..." popup, press L2+L3 to force close it
patch=1,EE,E003FFFF,extended,005D8280
patch=1,EE,E0020040,extended,008BDC10
patch=1,EE,E001FEFD,extended,0024BC1C
patch=1,EE,108BDC10,extended,00000000
```
#### Code file for emulator(.pnach)
[Download](./SLPM-66280_2F0E94A1_TeamLeaderPopupKiller.pnach)
#### Raw code
```
E003FFFF 005D8280
E0020040 008BDC10
E001FEFD 0024BC1C
108BDC10 00000000
```

## ItemBoxAnywhere
This feature is inspired by [dos-plus/dos-enhanced](https://greinoso96.github.io/mhplus-rel/index.html), big thanks to YuzucchiNyan.
* Press R2+L3 to open the item box anywhere in village or town.
* Item boxes opened in most public areas of the town can only be used to store or retrieve items, not to change equipment. This is specifically designed for online compatibility and is not a functional issue.
* The item box cannot be opened outside of the village/town, or when the player is unable to move freely | ready to depart for quest | interacting with other objects/characters.
* Equipment changed while visiting another player's house will only be broadcast to other players after leaving the house.
* In addition to the original game, the code is also theoretically compatible with the dos-plus/dos-enhanced patches created by YuzucchiNyan.
* Tested on PCSX2(v2.0 later) and PS2 fat 30000 model (OPL+PS2RD), with no issues found so far.

### Monster Hunter 2(dos) SLPM_662.80
#### Code for emulator
```
gametitle=Monster Hunter 2 (SLPM-66280)

[ItemBoxAnywhere(R2+L3)]
author=PoogieCharger
description=press R2+L3 to open item box anywhere in village or town
patch=1,EE,E030FFFF,extended,005D8280
patch=1,EE,E1060001,extended,005F9218
patch=1,EE,E0050000,extended,008BDC10
patch=1,EE,E004FDFD,extended,0024BC1C
patch=1,EE,205F91A0,extended,00802A48
patch=1,EE,E0020020,extended,0079CA24
patch=1,EE,E0013063,extended,0079CA26
patch=1,EE,2079CA24,extended,24030020
patch=1,EE,E1030000,extended,005F9218
patch=1,EE,E0020020,extended,0079CA24
patch=1,EE,E0012403,extended,0079CA26
patch=1,EE,2079CA24,extended,30630020
patch=1,EE,E0070C26,extended,00762622
patch=1,EE,E0060000,extended,00762624
patch=1,EE,20762620,extended,3C01008B
patch=1,EE,20762624,extended,8C224370
patch=1,EE,20762628,extended,0220282D
patch=1,EE,2076262C,extended,24060005
patch=1,EE,20762630,extended,0C0D52DC
patch=1,EE,20762634,extended,24440008
patch=1,EE,E1030083,extended,006ADCC4
patch=1,EE,E1020005,extended,007F1B77
patch=1,EE,007F1B77,extended,00000002
patch=1,EE,2076262C,extended,24060002
patch=1,EE,E1030084,extended,006ADCC4
patch=1,EE,E1020005,extended,007F1B77
patch=1,EE,007F1B77,extended,00000002
patch=1,EE,2076262C,extended,24060002
patch=1,EE,E1030086,extended,006ADCC4
patch=1,EE,E1020005,extended,007F1B77
patch=1,EE,007F1B77,extended,00000002
patch=1,EE,2076262C,extended,24060002
patch=1,EE,E1030087,extended,006ADCC4
patch=1,EE,E1020005,extended,007F1B77
patch=1,EE,007F1B77,extended,00000002
patch=1,EE,2076262C,extended,24060002
patch=1,EE,E1030088,extended,006ADCC4
patch=1,EE,E1020005,extended,007F1B77
patch=1,EE,007F1B77,extended,00000002
patch=1,EE,2076262C,extended,24060002
patch=1,EE,E0081112,extended,007F1B74
patch=1,EE,E0070209,extended,007F1B76
patch=1,EE,E1060083,extended,106ADCC4
patch=1,EE,E1050084,extended,106ADCC4
patch=1,EE,E1040086,extended,106ADCC4
patch=1,EE,E1030087,extended,106ADCC4
patch=1,EE,E1020088,extended,106ADCC4
patch=1,EE,007F1B77,extended,00000005
patch=1,EE,2076262C,extended,24060005
```
#### Code file for emulator(.pnach)
[Download](./SLPM-66280_2F0E94A1_ItemBoxAnywhere.pnach)
#### Raw code
```
E030FFFF 005D8280
E1060001 005F9218
E0050000 008BDC10
E004FDFD 0024BC1C
205F91A0 00802A48
E0020020 0079CA24
E0013063 0079CA26
2079CA24 24030020
E1030000 005F9218
E0020020 0079CA24
E0012403 0079CA26
2079CA24 30630020
E0070C26 00762622
E0060000 00762624
20762620 3C01008B
20762624 8C224370
20762628 0220282D
2076262C 24060005
20762630 0C0D52DC
20762634 24440008
E1030083 006ADCC4
E1020005 007F1B77
007F1B77 00000002
2076262C 24060002
E1030084 006ADCC4
E1020005 007F1B77
007F1B77 00000002
2076262C 24060002
E1030086 006ADCC4
E1020005 007F1B77
007F1B77 00000002
2076262C 24060002
E1030087 006ADCC4
E1020005 007F1B77
007F1B77 00000002
2076262C 24060002
E1030088 006ADCC4
E1020005 007F1B77
007F1B77 00000002
2076262C 24060002
E0081112 007F1B74
E0070209 007F1B76
E1060083 106ADCC4
E1050084 106ADCC4
E1040086 106ADCC4
E1030087 106ADCC4
E1020088 106ADCC4
007F1B77 00000005
2076262C 24060005
```

## SaveState2MemCard
This is intended solely to bypass the game's built-in verification function that prevents save states from being saved to the memcard in certain conditions. It is not meant to encourage abuse of the save state feature.
* Only enable "Enable SaveState2MemCard" when necessary, and make sure to back up your memcard in advance. After successfully saving, it is strongly recommended to disable the code, then activate "Disable SaveState2MemCard" once, let the game resume running, and then turn off "Disable SaveState2MemCard".
* This code does not perform saving by itself; you still need to manually execute the game's save action.
* The game's built-in verification function ensures that save data cannot be written to another memcard/save data. Activating the code bypasses this safety mechanism, so there is a certain risks--one may accidentally overwrite existing save data on the memcard due to misoperation.
* For MH1j/MHG, saving will write all 3 characters to the 3 slots of the memcard save file. For MH2, only the currently used character will be saved to the current slot of the memcard save file.

### Monster Hunter(1j) SLPM_654.95
#### Code for emulator
```
gametitle=Monster Hunter (SLPM-65495)

[Enable SaveState2MemCard]
author=PoogieCharger
description=CAUTION! Can save with any SaveStates, only enable this when you REALLY need to save
patch=1,EE,10284A12,extended,00001000

[Disable SaveState2MemCard]
author=PoogieCharger
description=disable "Enable SaveState2MemCard" first, then enable "Disable SaveState2MemCard", resume game, then you can disable this, too
patch=1,EE,10284A12,extended,00001440
```
#### Code file for emulator(.pnach)
[Download](./SLPM-65495_C2008A92_SaveState2MemCard.pnach)

### Monster Hunter G SLPM_658.69
#### Code for emulator
```
gametitle=Monster Hunter G (SLPM-65869)

[Enable SaveState2MemCard]
author=PoogieCharger
description=CAUTION! Can save with any SaveStates, only enable this when you REALLY need to save
patch=1,EE,1022E9F2,extended,00001000

[Disable SaveState2MemCard]
author=PoogieCharger
description=disable "Enable SaveState2MemCard" first, then enable "Disable SaveState2MemCard", resume game, then you can disable this, too
patch=1,EE,1022E9F2,extended,00001440
```
#### Code file for emulator(.pnach)
[Download](./SLPM-65869_29396A53_SaveState2MemCard.pnach)

### Monster Hunter 2(dos) SLPM_662.80
#### Code for emulator
```
gametitle=Monster Hunter 2 (SLPM-66280)

[Enable SaveState2MemCard]
author=PoogieCharger
description=CAUTION! Can save with any SaveStates, only enable this when you REALLY need to save
patch=1,EE,203DB240,extended,00000000

[Disable SaveState2MemCard]
author=PoogieCharger
description=disable "Enable SaveState2MemCard" first, then enable "Disable SaveState2MemCard", resume game, then you can disable this, too
patch=1,EE,203DB240,extended,10400021
```
#### Code file for emulator(.pnach)
[Download](./SLPM-66280_2F0E94A1_SaveState2MemCard.pnach)

## PSP Connection Check Bypass

### Monster Hunter 2(dos) SLPM_662.80
Enter *CONNECT* from main menu, load your save and get ready, on *Checking MONSTER HUNTER PORTABLE* screen, press *SELECT+START* to bypass the connection check.

* Support PCSX2 mordern cheat system, can be toggled on/off
* Key combination only takes effect on checking connection screen(a total three conditional checks for actual execution), it can theoretically remain on without other effects
* Theoretically the same as connecting with a real PSP
* Tested on PCSX2(v2.0 later) and PS2 fat 30000 model (OPL+PS2RD), not guaranteed for other envrionments
#### Code for emulator
```
gametitle=Monster Hunter 2 (SLPM-66280)

[PSP Connection Check Bypass(SELECT+START)]
author=PoogieCharger
description=Press SELECT+START to bypass connection check with Monster Hunter Portable.
patch=1,EE,E0040002,extended,00AC8158
patch=1,EE,E003000B,extended,00AC8154
patch=1,EE,E002FFF6,extended,0024BC1C
patch=1,EE,10AC95C0,extended,00000FFF
patch=1,EE,00AC8100,extended,00000001
```
#### Code file for emulator(.pnach)
[Download](./SLPM-66280_2F0E94A1_PSP_Connection_Check_Bypass.pnach)
#### Raw code
```
E0040002 00AC8158
E003000B 00AC8154
E002FFF6 0024BC1C
10AC95C0 00000FFF
00AC8100 00000001
```

# PSP

## PS2 Connection Check Bypass

### Monster Hunter Portable(MHP) ULJM-05066
Enter *CONNECT* from main menu, load your save and get ready, on *Checking MONSTER HUNTER 2* screen, press *SELECT+START* to bypass the connection check.

* Cannot prevent repeated triggering(for now), please don't press the key combination outside the CONNECT screen, or just disable the code when not in use;
* Theoretically the same as connecting with a real PS2(MH2 progress having completed the slaying of Kushala Daora);
* Tested on PPSSPP(v1.19.3) and PSP 3000 model(Ark-4 cfw+Cheat Master Fusion), not guaranteed for other envrionments.
#### Code for emulator
```
_C1 PS2 Connection Check Bypass(SELECT+START)
Press SELECT+START to bypass connection check with Monster Hunter 2.
_L 0xE0030009 0x00179E94
_L 0xE0020001 0x00224848
_L 0x102248C0 0x00003F2F
_L 0x00224848 0x00000003
```
#### Code file for emulator(.ini)
[Download](./ULJM05066_PS2_Connection_Check_Bypass.ini)


###### Last update: 2026/05/05 by PoogieCharger
