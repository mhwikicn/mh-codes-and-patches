# 怪物猎人相关代码补丁文件

#### 多为金手指代码，可用于模拟器或具有功能完善的金手指引擎的实机

# PS2
## 怪物猎人2（dos） SLPM_662.80

### PSP联动检测绕过

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
## 怪物猎人便携版（MHP） ULJM-05066

### PS2联动检测绕过

进入主菜单的 *CONNECT* 界面，读档并准备完毕，等待确认 *MONSTER HUNTER 2* 连接时，按下 *SELECT+START* 可绕过连接检测直接实现成功联动。

* 暂时没有好的的防重复触发方案，在非联动界面尽量不要使用触发组合键，或者在无需联动时关闭该代码；
* 理论上效果等同于和PS2实机联动；
* 已通过PPSSPP模拟器（v1.19.3）和PSP3000机型（ARK-4自制系统+CMF金手指引擎）测试，其他环境未测试，不保证能够正常工作。
#### 模拟器专用代码文本
```
_C1 PS2联动检测绕过(SELECT+START)
在联动界面检测MH2连接时，按SELECT+START绕过检测
_L 0xE0030009 0x00179e94
_L 0xE0020001 0x00224848
_L 0x102248C0 0x000039FF
_L 0x00224848 0x00000003

```
#### 模拟器专用代码文件（.ini后缀）
[下载](./ULJM05066_PS2联动检测绕过.ini)


###### 最后更新: 2025/12/20 by 猪突猛进锅
