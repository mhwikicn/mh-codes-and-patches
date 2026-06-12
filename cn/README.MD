# 怪物猎人相关代码补丁文件

#### 多为金手指代码，可用于模拟器或具有功能完善的金手指引擎的实机

# PS2

## 输入法优化
优化了切换到英文输入时的默认状态，改为使用半角小写字符，而非使用全角字符甚至大写字母（说的就是你，怪物猎人1j），在重新打开输入窗口时会保持上一次的输入状态，无需频繁切换输入法。
* 发送快捷聊天或动作后，再次打开聊天窗口时的输入状态取决于上一个非快捷聊天/动作的输入状态。
* 对于打上了已经设置默认输入为英文状态的补丁的版本（MHG/MH2），这份代码用途就不大了，而且可能不会按预期工作。
* 需要使用新版PCSX2模拟器（v2.0以上），或者自行编辑添加到原有的pnach代码文件中。

### 怪物猎人（1j） SLPM_654.95
#### 模拟器专用代码文本
```
gametitle=Monster Hunter (SLPM-65495)

[输入法优化]
author=猪突猛进锅
description=优化英文默认输入模式(半角小写)以及输入法状态记忆功能
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
#### 模拟器专用代码文件（.pnach后缀，独立版）
[下载](./SLPM-65495_C2008A92_输入法优化.pnach)
#### 原始码
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

### 怪物猎人G SLPM_658.69
#### 模拟器专用代码文本
```
gametitle=Monster Hunter G (SLPM-65869)

[输入法优化]
author=猪突猛进锅
description=优化英文默认输入模式以及输入法状态记忆功能
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
#### 模拟器专用代码文件（.pnach后缀，独立版）
[下载](./SLPM-65869_29396A53_输入法优化.pnach)
#### 原始码
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

### 怪物猎人2（dos） SLPM_662.80
#### 模拟器专用代码文本
```
gametitle=Monster Hunter 2 (SLPM-66280)

[输入法优化]
author=猪突猛进锅
description=优化英文默认输入模式以及输入法状态记忆功能
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
#### 模拟器专用代码文件（.pnach后缀，独立版）
[下载](./SLPM-66280_2F0E94A1_输入法优化.pnach)
#### 原始码
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

## 远程武器视角锁定
原版游戏使用远程武器瞄准时，取消瞄准状态（弩：松开L1，弓：松开R1）后，会自动根据瞄准视角调整视角高度，该代码可设置锁定视角高度，不受远程武器瞄准影响。
* 按 START + → 开启功能，按 START + ← 关闭并恢复原版状态。
* 需要使用新版PCSX2模拟器（v2.0以上），或者自行编辑添加到原有的pnach代码文件中。

### 怪物猎人2（dos） SLPM_662.80
#### 模拟器专用代码文本
```
gametitle=Monster Hunter 2 (SLPM-66280)

[远程武器视角锁定]
author=猪突猛进锅
description=使用远程武器瞄准后恢复至普通视角（弩：松开L1，弓：松开R1）时，可维持瞄准前的视角高度，START + →开启，START + ←关闭
patch=1,EE,D024BC1C,extended,0300FFD7
patch=1,EE,D031B1B0,extended,02000070
patch=1,EE,D031B1B2,extended,0100A264
patch=1,EE,2031B1B0,extended,00000000
patch=1,EE,D024BC1C,extended,0300FF77
patch=1,EE,D031B1B0,extended,02000000
patch=1,EE,D031B1B2,extended,01000000
patch=1,EE,2031B1B0,extended,A2640070
```
#### 模拟器专用代码文件（.pnach后缀，独立版）
[下载](./SLPM-66280_2F0E94A1_远程武器视角锁定.pnach)
#### 原始码
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

## 关闭领导者弹窗
MH2目前在线上模式时有时会出现“领导者正在…”的弹窗，导致无法正常游戏，在多人PvP不能正常进行的情况下，可以按L2+L3关闭该弹窗，理论上不会有其他影响。
* 如果未来服务器支持多人PvP，这一弹窗出现不再是问题时，请考虑禁用代码，或避免按下组合键，并仅在出现非正常弹窗时按下组合键。
* 需要使用新版PCSX2模拟器（v2.0以上），或者自行编辑添加到原有的pnach代码文件中。

### 怪物猎人2（dos） SLPM_662.80
#### 模拟器专用代码文本
```
gametitle=Monster Hunter 2 (SLPM-66280)

[关闭“领导者正在…”弹窗(L2+L3)]
author=猪突猛进锅
description=某些情况下弹出“领导者正在…”窗口时，按L2+L3可将其关闭
patch=1,EE,E003FFFF,extended,005D8280
patch=1,EE,E0020040,extended,008BDC10
patch=1,EE,E001FEFD,extended,0024BC1C
patch=1,EE,108BDC10,extended,00000000
```
#### 模拟器专用代码文件（.pnach后缀，独立版）
[下载](./SLPM-66280_2F0E94A1_关闭领导者弹窗.pnach)
#### 原始码
```
E003FFFF 005D8280
E0020040 008BDC10
E001FEFD 0024BC1C
108BDC10 00000000
```

## 随身箱子
该功能受[dos-plus/dos-enhanced](https://greinoso96.github.io/mhplus-rel/index.html)的启发而制作，向YuzucchiNyan致谢。
* 按R2+L3可在村中或城镇任意地点打开物品箱。
* 在城镇大部分公共地区打开的物品箱仅能用于存取物品，不能更换装备，这是为了联机兼容性专门设置的，并非功能问题。
* 在非城镇或村中/玩家无法自由行动/玩家已准备任务出发/玩家与其他对象交互中时无法打开箱子。
* 在其他人家中做客时更换的装备只会在出门后广播到其他玩家。
* 除支持原版游戏，代码理论上也兼容YuzucchiNyan制作的dos-plus与dos-enhanced补丁。
* 已通过PCSX2模拟器（v2.0以上新版）和PS2厚机30000机型（OPL+PS2RD金手指引擎）测试，目前未发现问题。

### 怪物猎人2（dos） SLPM_662.80
#### 模拟器专用代码文本
```
gametitle=Monster Hunter 2 (SLPM-66280)

[随身箱子(R2+L3)]
author=猪突猛进锅
description=在村子或城镇中按R2+L3打开箱子界面
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
#### 模拟器专用代码文件（.pnach后缀，独立版）
[下载](./SLPM-66280_2F0E94A1_随身箱子.pnach)
#### 原始码
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

## 即时存档强制保存
本代码仅用于解决游戏内置的校验功能导致即时存档无法保存到记忆卡的问题，并不鼓励滥用即时存档功能。
* 仅在需要时开启“启用即时存档强制保存”，并提前做好记忆卡备份，成功保存后强烈建议关闭该代码，并激活一次“禁用即时存档强制保存”，恢复游戏运行后再关闭“禁用即时存档强制保存”。
* 本代码不会直接进行保存，仍然需要你手动执行游戏的保存动作。
* 游戏内置的校验功能是为了确保存档不会被写入其他的记忆卡/存档中，激活强制保存将跳过这一安全机制，因此存在一定的风险，可能会因误操作覆盖记忆卡中原有的存档。
* 对于MH1j/MHG，保存时会将3个角色全部保存到记忆卡存档的3个栏位；对于MH2，则只会保存当前使用的角色到记忆卡存档的当前栏位。

### 怪物猎人（1j） SLPM_654.95
#### 模拟器专用代码文本
```
gametitle=Monster Hunter (SLPM-65495)

[启用即时存档强制保存]
author=猪突猛进锅
description=注意! 能够保存任意即时存档到记忆卡中，请仅在需要的时候开启
patch=1,EE,10284A12,extended,00001000

[禁用即时存档强制保存]
author=猪突猛进锅
description=先关闭“启用即时存档强制保存”，再开启“禁用即时存档强制保存”，恢复游戏后，就可以关闭“禁用即时存档强制保存”了
patch=1,EE,10284A12,extended,00001440
```
#### 模拟器专用代码文件（.pnach后缀，独立版）
[下载](./SLPM-65495_C2008A92_即时存档强制保存.pnach)

### 怪物猎人G SLPM_658.69
#### 模拟器专用代码文本
```
gametitle=Monster Hunter G (SLPM-65869)

[启用即时存档强制保存]
author=猪突猛进锅
description=注意! 能够保存任意即时存档到记忆卡中，请仅在需要的时候开启
patch=1,EE,1022E9F2,extended,00001000

[禁用即时存档强制保存]
author=猪突猛进锅
description=先关闭“启用即时存档强制保存”，再开启“禁用即时存档强制保存”，恢复游戏后，就可以关闭“禁用即时存档强制保存”了
patch=1,EE,1022E9F2,extended,00001440
```
#### 模拟器专用代码文件（.pnach后缀，独立版）
[下载](./SLPM-65869_29396A53_即时存档强制保存.pnach)

### 怪物猎人2（dos） SLPM_662.80
#### 模拟器专用代码文本
```
gametitle=Monster Hunter 2 (SLPM-66280)

[启用即时存档强制保存]
author=猪突猛进锅
description=注意! 能够保存任意即时存档到记忆卡中，请仅在需要的时候开启
patch=1,EE,203DB240,extended,00000000

[禁用即时存档强制保存]
author=猪突猛进锅
description=先关闭“启用即时存档强制保存”，再开启“禁用即时存档强制保存”，恢复游戏后，就可以关闭“禁用即时存档强制保存”了
patch=1,EE,203DB240,extended,10400021
```
#### 模拟器专用代码文件（.pnach后缀，独立版）
[下载](./SLPM-66280_2F0E94A1_即时存档强制保存.pnach)

## PSP联动检测绕过

### 怪物猎人2（dos） SLPM_662.80
进入主菜单的 *CONNECT* 界面，读档并准备完毕，等待确认 *MONSTER HUNTER PORTABLE* 连接时，按下 *SELECT+START* 可绕过连接检测直接实现成功联动。

* 支持PCSX2新版金手指系统，可开关切换；
* 按键组合触发只会在联动界面生效(一共需要满足三个条件才会执行)，理论上可以保持常开，没有其他影响；
* 理论上效果等同于和PSP实机联动；
* 已通过PCSX2模拟器（v2.0以上新版）和PS2厚机30000机型（OPL+PS2RD金手指引擎）测试，其他环境未测试，不保证能够正常工作。
#### 模拟器专用代码文本
```
gametitle=Monster Hunter 2 (SLPM-66280)

[PSP联动检测绕过(SELECT+START)]
author=猪突猛进锅
description=在联动界面检测MHP连接时，按SELECT+START绕过检测
patch=1,EE,E0040002,extended,00AC8158
patch=1,EE,E003000B,extended,00AC8154
patch=1,EE,E002FFF6,extended,0024BC1C
patch=1,EE,10AC95C0,extended,00000FFF
patch=1,EE,00AC8100,extended,00000001
```
#### 模拟器专用代码文件（.pnach后缀，独立版）
[下载](./SLPM-66280_2F0E94A1_PSP联动检测绕过.pnach)
#### 原始码
```
E0040002 00AC8158
E003000B 00AC8154
E002FFF6 0024BC1C
10AC95C0 00000FFF
00AC8100 00000001
```

# PSP

## PS2联动检测绕过

### 怪物猎人便携版（MHP） ULJM-05066
进入主菜单的 *CONNECT* 界面，读档并准备完毕，等待确认 *MONSTER HUNTER 2* 连接时，按下 *SELECT+START* 可绕过连接检测直接实现成功联动。

* 暂时没有好的的防重复触发方案，在非联动界面尽量不要使用触发组合键，或者在无需联动时关闭该代码；
* 理论上效果等同于和PS2实机（MH2游戏进度已完成讨伐钢龍）联动；
* 已通过PPSSPP模拟器（v1.19.3）和PSP3000机型（ARK-4自制系统+CMF金手指引擎）测试，其他环境未测试，不保证能够正常工作。
#### 模拟器专用代码文本
```
_C1 PS2联动检测绕过(SELECT+START)
在联动界面检测MH2连接时，按SELECT+START绕过检测
_L 0xE0030009 0x00179E94
_L 0xE0020001 0x00224848
_L 0x102248C0 0x00003FFF
_L 0x00224848 0x00000003
```
#### 模拟器专用代码文件（.ini后缀）
[下载](./ULJM05066_PS2联动检测绕过.ini)


###### 最后更新: 2026/06/12 by 猪突猛进锅
