# 128k RAM expansion for the ZX Spectrum 48k

![image](/Images/rev2.jpg)
<br/>

Upgrade ZX Spectrum 48k with 128kB of RAM and play games you couldn't play before. Sound will stay as before, but you can always build an [AY interface](https://github.com/goloskokovic/zx16to128upgrade/tree/main/AY) to sound like ZX Spectrum 128k. No need to change the ROM.

In order to make the RAM expansion work, a single wire mod to your ZX Spectrum 48k is required to disable the 32k upper RAM.
For Issue 2/3/4 connect pin 5 on IC23 (74LS32) to pin 14 (+5V). For Issue 5/6 connect pin 35 on IC27 (ZX8401) to pin 40 (+5V).
Both mods will hold the CAS/RAS signal high so it won't reach the RAM chips.
<br/>

Watch the video:

[![Watch the video](https://img.youtube.com/vi/-c24jNaIezs/default.jpg)](https://www.youtube.com/watch?v=-c24jNaIezs&t=853s)




![image](/Images/CAS.png)

With this mod without the RAM expansion, your ZX Spectrum 48k will work as ZX Spectrum 16k.

To test the RAM expansion use modified [zx-diagnostics](/testram.tap) that allows you to manually select 128k test regardless of the ROM.

<br/>
<br/>
<br/>

![image](/Images/brd.png)

<br/>
<br/>
GAL equations:

```
when 74HCT273_CLK is CLK7FFD
D0 is BANK0
D1 is BANK1
D2 is BANK2

CLK7FFD = /IORQ*/WR*/A15*A5*/A1
/RAMCS = /MREQ*A15
SA14 = A14*A15*BANK0
SA15 = A14*A15*BANK1 + /A14*A15
SA16 = A14*A15*BANK2
```
Original page: https://velesoft.speccy.cz/zx/external_128kb_upgrade/index.htm
