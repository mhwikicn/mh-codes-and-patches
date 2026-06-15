# Monster Hunter code and patches

#### Mostly cheat code, for emulators or real hardware system with a proper cheat support.

# PS2

## InputMethodOptimization
Optimized the default state when switching to English input mode: it now uses half‑width lowercase characters by default, instead of full‑width characters or even uppercase letters (yes, I'm looking at you, Monster Hunter 1j). When the input window is reopened, the previous input state is retained, so you don't need to keep switching input methods.
* After sending a quick chat or an action, the input state when reopening the chat window depends on the last non‑quick‑chat / non‑action input state.
* For versions that already have a patch setting English input as the default (e.g., MHG / MH2 with English patch), this code is of little use and may not work as expected.
* Requires the newer version of PCSX2 emulator (v2.0 or later), or you can manually edit and add the code to your existing .pnach file.

### Monster Hunter(1j) SLPM_654.95
#### Code for emulator
```
gametitle=Monster Hunter (SLPM-65495)

[InputMethodOptimization]
author=PoogieCharger
description=Set the English input mode to use (half-width, lowercase) as default, and optimize the input method to retain previous state.
patch=1,EE,200F0000,extended,3C010052
patch=1,EE,200F0004,extended,2421EEAF
patch=1,EE,200F0008,extended,14A10015
patch=1,EE,200F000C,extended,24090002
patch=1,EE,200F0010,extended,50890016
patch=1,EE,200F0014,extended,2404000F
patch=1,EE,200F0018,extended,24090004
patch=1,EE,200F001C,extended,240B0005
patch=1,EE,200F0020,extended,14890008
patch=1,EE,200F0024,extended,3C01000F
patch=1,EE,200F0028,extended,90A90000
patch=1,EE,200F002C,extended,112B000C
patch=1,EE,200F0030,extended,00000000
patch=1,EE,200F0034,extended,A029FFFF
patch=1,EE,200F0038,extended,90C90000
patch=1,EE,200F003C,extended,10000008
patch=1,EE,200F0040,extended,A029FFFE
patch=1,EE,200F0044,extended,148B0006
patch=1,EE,200F0048,extended,90AB0000
patch=1,EE,200F004C,extended,112B0004
patch=1,EE,200F0050,extended,00000000
patch=1,EE,200F0054,extended,A02BFFFF
patch=1,EE,200F0058,extended,90C90000
patch=1,EE,200F005C,extended,A029FFFE
patch=1,EE,200F0060,extended,A0A40000
patch=1,EE,200F0064,extended,080988D0
patch=1,EE,200F0068,extended,A0C40000
patch=1,EE,200F006C,extended,A0A90000
patch=1,EE,200F0070,extended,080988D0
patch=1,EE,200F0074,extended,A0C40000
patch=1,EE,200F0078,extended,8F82BB60
patch=1,EE,200F007C,extended,9049001E
patch=1,EE,200F0080,extended,240A0004
patch=1,EE,200F0084,extended,152A0003
patch=1,EE,200F0088,extended,240A0005
patch=1,EE,200F008C,extended,10000002
patch=1,EE,200F0090,extended,00000000
patch=1,EE,200F0094,extended,152A0005
patch=1,EE,200F0098,extended,3C01000F
patch=1,EE,200F009C,extended,9029FFFE
patch=1,EE,200F00A0,extended,A049001E
patch=1,EE,200F00A4,extended,9029FFFF
patch=1,EE,200F00A8,extended,A049001F
patch=1,EE,200F00AC,extended,08097F32
patch=1,EE,200F00B0,extended,00000000
patch=1,EE,D025FCC0,extended,0A00BB60
patch=1,EE,D025FCC2,extended,09008F82
patch=1,EE,D0262338,extended,08000000
patch=1,EE,D026233A,extended,0700A0A4
patch=1,EE,2025FB1C,extended,00000000
patch=1,EE,2025FCB8,extended,00000000
patch=1,EE,2025FCC0,extended,0803C01E
patch=1,EE,2025FCC4,extended,00000000
patch=1,EE,20262338,extended,0803C000
patch=1,EE,2026233C,extended,00000000
patch=1,EE,2026248C,extended,00000000
```
#### Code file for emulator(.pnach)
[Download](./SLPM-65495_C2008A92_InputMethodOptimization.pnach)
#### Raw code
```
200F0000 3C010052
200F0004 2421EEAF
200F0008 14A10015
200F000C 24090002
200F0010 50890016
200F0014 2404000F
200F0018 24090004
200F001C 240B0005
200F0020 14890008
200F0024 3C01000F
200F0028 90A90000
200F002C 112B000C
200F0030 00000000
200F0034 A029FFFF
200F0038 90C90000
200F003C 10000008
200F0040 A029FFFE
200F0044 148B0006
200F0048 90AB0000
200F004C 112B0004
200F0050 00000000
200F0054 A02BFFFF
200F0058 90C90000
200F005C A029FFFE
200F0060 A0A40000
200F0064 080988D0
200F0068 A0C40000
200F006C A0A90000
200F0070 080988D0
200F0074 A0C40000
200F0078 8F82BB60
200F007C 9049001E
200F0080 240A0004
200F0084 152A0003
200F0088 240A0005
200F008C 10000002
200F0090 00000000
200F0094 152A0005
200F0098 3C01000F
200F009C 9029FFFE
200F00A0 A049001E
200F00A4 9029FFFF
200F00A8 A049001F
200F00AC 08097F32
200F00B0 00000000
E00ABB60 0025FCC0
E0098F82 0025FCC2
E0080000 00262338
E007A0A4 0026233A
2025FB1C 00000000
2025FCB8 00000000
2025FCC0 0803C01E
2025FCC4 00000000
20262338 0803C000
2026233C 00000000
2026248C 00000000
```

### Monster Hunter G SLPM_658.69
#### Code for emulator
```
gametitle=Monster Hunter G (SLPM-65869)

[InputMethodOptimization]
author=PoogieCharger
description=Set the English input mode to use half-width as default, and optimize the input method to retain previous state.
patch=1,EE,200F0000,extended,3C010042
patch=1,EE,200F0004,extended,2421D9CF
patch=1,EE,200F0008,extended,14A10015
patch=1,EE,200F000C,extended,2409000A
patch=1,EE,200F0010,extended,50890016
patch=1,EE,200F0014,extended,2404000F
patch=1,EE,200F0018,extended,24090004
patch=1,EE,200F001C,extended,240B0005
patch=1,EE,200F0020,extended,14890008
patch=1,EE,200F0024,extended,3C01000F
patch=1,EE,200F0028,extended,90A90000
patch=1,EE,200F002C,extended,112B000C
patch=1,EE,200F0030,extended,00000000
patch=1,EE,200F0034,extended,A029FFFF
patch=1,EE,200F0038,extended,90C90000
patch=1,EE,200F003C,extended,10000008
patch=1,EE,200F0040,extended,A029FFFE
patch=1,EE,200F0044,extended,148B0006
patch=1,EE,200F0048,extended,90AB0000
patch=1,EE,200F004C,extended,112B0004
patch=1,EE,200F0050,extended,00000000
patch=1,EE,200F0054,extended,A02BFFFF
patch=1,EE,200F0058,extended,90C90000
patch=1,EE,200F005C,extended,A029FFFE
patch=1,EE,200F0060,extended,A0A40000
patch=1,EE,200F0064,extended,08082EF2
patch=1,EE,200F0068,extended,A0C40000
patch=1,EE,200F006C,extended,A0A90000
patch=1,EE,200F0070,extended,08082EF2
patch=1,EE,200F0074,extended,A0C40000
patch=1,EE,200F0078,extended,24A9001E
patch=1,EE,200F007C,extended,10C9000E
patch=1,EE,200F0080,extended,24090004
patch=1,EE,200F0084,extended,90AA001F
patch=1,EE,200F0088,extended,152A0003
patch=1,EE,200F008C,extended,24090005
patch=1,EE,200F0090,extended,10000002
patch=1,EE,200F0094,extended,00000000
patch=1,EE,200F0098,extended,152A0005
patch=1,EE,200F009C,extended,3C01000F
patch=1,EE,200F00A0,extended,9029FFFE
patch=1,EE,200F00A4,extended,A0A9001E
patch=1,EE,200F00A8,extended,9029FFFF
patch=1,EE,200F00AC,extended,A0A9001F
patch=1,EE,200F00B0,extended,08082F46
patch=1,EE,200F00B4,extended,00000000
patch=1,EE,200F00B8,extended,00641821
patch=1,EE,200F00BC,extended,90630000
patch=1,EE,200F00C0,extended,08082F46
patch=1,EE,200F00C4,extended,A0A3001F
patch=1,EE,200F00C8,extended,00000000
patch=1,EE,D020BBC0,extended,0A000000
patch=1,EE,D020BBC2,extended,0900A0A4
patch=1,EE,D020BD10,extended,08001821
patch=1,EE,D020BD12,extended,07000064
patch=1,EE,20208FA8,extended,00000000
patch=1,EE,2020922C,extended,00000000
patch=1,EE,2020BBC0,extended,0803C000
patch=1,EE,2020BBC4,extended,00000000
patch=1,EE,2020BD10,extended,0803C01E
patch=1,EE,2020BD14,extended,00000000
patch=1,EE,2020BD1C,extended,00000000
```
#### Code file for emulator(.pnach)
[Download](./SLPM-65869_29396A53_InputMethodOptimization.pnach)
#### Raw code
```
200F0000 3C010042
200F0004 2421D9CF
200F0008 14A10015
200F000C 2409000A
200F0010 50890016
200F0014 2404000F
200F0018 24090004
200F001C 240B0005
200F0020 14890008
200F0024 3C01000F
200F0028 90A90000
200F002C 112B000C
200F0030 00000000
200F0034 A029FFFF
200F0038 90C90000
200F003C 10000008
200F0040 A029FFFE
200F0044 148B0006
200F0048 90AB0000
200F004C 112B0004
200F0050 00000000
200F0054 A02BFFFF
200F0058 90C90000
200F005C A029FFFE
200F0060 A0A40000
200F0064 08082EF2
200F0068 A0C40000
200F006C A0A90000
200F0070 08082EF2
200F0074 A0C40000
200F0078 24A9001E
200F007C 10C9000E
200F0080 24090004
200F0084 90AA001F
200F0088 152A0003
200F008C 24090005
200F0090 10000002
200F0094 00000000
200F0098 152A0005
200F009C 3C01000F
200F00A0 9029FFFE
200F00A4 A0A9001E
200F00A8 9029FFFF
200F00AC A0A9001F
200F00B0 08082F46
200F00B4 00000000
200F00B8 00641821
200F00BC 90630000
200F00C0 08082F46
200F00C4 A0A3001F
200F00C8 00000000
E00A0000 0020BBC0
E009A0A4 0020BBC2
E0081821 0020BD10
E0070064 0020BD12
20208FA8 00000000
2020922C 00000000
2020BBC0 0803C000
2020BBC4 00000000
2020BD10 0803C01E
2020BD14 00000000
2020BD1C 00000000
```

### Monster Hunter 2(dos) SLPM_662.80
#### Code for emulator
```
gametitle=Monster Hunter 2 (SLPM-66280)

[InputMethodOptimization]
author=PoogieCharger
description=Set the English input mode to use half-width as default, and optimize the input method to retain previous state.
patch=1,EE,200F0000,extended,3C01005B
patch=1,EE,200F0004,extended,2421EABF
patch=1,EE,200F0008,extended,14A10006
patch=1,EE,200F000C,extended,2409000A
patch=1,EE,200F0010,extended,14890004
patch=1,EE,200F0014,extended,2409000F
patch=1,EE,200F0018,extended,A0C90000
patch=1,EE,200F001C,extended,080C663C
patch=1,EE,200F0020,extended,A0A40000
patch=1,EE,200F0024,extended,A0C40000
patch=1,EE,200F0028,extended,080C663C
patch=1,EE,200F002C,extended,A0A40000
patch=1,EE,200F0030,extended,24090004
patch=1,EE,200F0034,extended,10690008
patch=1,EE,200F0038,extended,24090005
patch=1,EE,200F003C,extended,10690006
patch=1,EE,200F0040,extended,2409000D
patch=1,EE,200F0044,extended,10690004
patch=1,EE,200F0048,extended,3C01000F
patch=1,EE,200F004C,extended,A023FFFF
patch=1,EE,200F0050,extended,A024FFFE
patch=1,EE,200F0054,extended,A0A4FFA0
patch=1,EE,200F0058,extended,03E00008
patch=1,EE,200F005C,extended,A0A3001F
patch=1,EE,200F0060,extended,3C09000F
patch=1,EE,200F0064,extended,9129FFFE
patch=1,EE,200F0068,extended,080C54CC
patch=1,EE,200F006C,extended,A029EA40
patch=1,EE,D031531C,extended,09000004
patch=1,EE,D031531E,extended,08001000
patch=1,EE,D03198E8,extended,07000000
patch=1,EE,D03198EA,extended,0600A0A4
patch=1,EE,2031531C,extended,0803C018
patch=1,EE,20315320,extended,00000000
patch=1,EE,203198E8,extended,0803C000
patch=1,EE,203198EC,extended,00000000
patch=1,EE,20319A4C,extended,0803C00C
patch=1,EE,20319A50,extended,00000000
```
#### Code file for emulator(.pnach)
[Download](./SLPM-66280_2F0E94A1_InputMethodOptimization.pnach)
#### Raw code
```
200F0000 3C01005B
200F0004 2421EABF
200F0008 14A10006
200F000C 2409000A
200F0010 14890004
200F0014 2409000F
200F0018 A0C90000
200F001C 080C663C
200F0020 A0A40000
200F0024 A0C40000
200F0028 080C663C
200F002C A0A40000
200F0030 24090004
200F0034 10690008
200F0038 24090005
200F003C 10690006
200F0040 2409000D
200F0044 10690004
200F0048 3C01000F
200F004C A023FFFF
200F0050 A024FFFE
200F0054 A0A4FFA0
200F0058 03E00008
200F005C A0A3001F
200F0060 3C09000F
200F0064 9129FFFE
200F0068 080C54CC
200F006C A029EA40
E0090004 0031531C
E0081000 0031531E
E0070000 003198E8
E006A0A4 003198EA
2031531C 0803C018
20315320 00000000
203198E8 0803C000
203198EC 00000000
20319A4C 0803C00C
20319A50 00000000
```

## RangedWeaponCameraLock
In the original game, when aiming with a ranged weapon and then canceling the aim (bowgun: release L1, bow: release R1), the camera height automatically adjusts based on the aiming view. This code allows you to lock the camera height so it is not affected by ranged weapon aiming.
* Press START + → to enable the function, press START + ← to disable and revert to the original behavior.
* Requires the newer version of PCSX2 emulator (v2.0 or later), or you can manually edit and add the code to your existing .pnach file.

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
* If the server supports multiplayer PvP in the future and this popup window is no longer an issue, please consider disabling the code or avoid pressing the button combination, and only press it when an abnormal popup window appears.
* Requires the newer version of PCSX2 emulator (v2.0 or later), or you can manually edit and add the code to your existing .pnach file.

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
* Button combination only takes effect on checking connection screen(a total three conditional checks for actual execution), it can theoretically remain on without other effects
* Theoretically the same as connecting with a real PSP
* Tested on PCSX2(v2.0 later) and PS2 fat 30000 model (OPL+PS2RD), not guaranteed for other environments
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

* Cannot prevent repeated triggering(for now), please don't press the button combination outside the CONNECT screen, or just disable the code when not in use;
* Theoretically the same as connecting with a real PS2(MH2 progress having completed the slaying of Kushala Daora);
* Tested on PPSSPP(v1.19.3) and PSP 3000 model(Ark-4 cfw+Cheat Master Fusion), not guaranteed for other environments.
#### Code for emulator
```
_C1 PS2 Connection Check Bypass(SELECT+START)
Press SELECT+START to bypass connection check with Monster Hunter 2.
_L 0xE0030009 0x00179E94
_L 0xE0020001 0x00224848
_L 0x102248C0 0x00003FFF
_L 0x00224848 0x00000003
```
#### Code file for emulator(.ini)
[Download](./ULJM05066_PS2_Connection_Check_Bypass.ini)


###### Last update: 2026/06/12 by PoogieCharger
