# 128k RAM expansion for ZX 48k
Upgrade ZX Spectrum 48k with 128kB of RAM and play all the games you couldn't play before. The sound will stay as before, but you can always build an [AY interface](https://github.com/konkotgit/KAY-Kempston-AY) to sound like ZX Spectrum 128k.

In order to make the RAM expansion work, an "one wire mod" to your ZX Spectrum 48k is required to disable the 32k upper RAM.
For Issue 2/3/4 connect pin 5 on IC23 (74LS32) to pin 14 (+5V). For Issue 5/6 connect pin 35 on IC27 (ZX8401) to pin 40 (+5V).
Both mods will hold the CAS/RAS signal high so it won't reach the RAM chips.

https://spectrumcomputing.co.uk/forums/viewtopic.php?t=2616

<br/>


![image](/Images/CAS.png)

With this mod without the RAM expansion, your ZX Spectrum 48k will work as ZX Spectrum 16k. No need to change the ROM.

To test the RAM expansion use modified [zx-diagnostics](/testram.tap) that allows you to manually select 128k test regardless of the ROM.

<br/>
<br/>
<br/>

![image](/Images/brd.png)

![image](/Images/rev2.jpg)


Original page: https://velesoft.speccy.cz/zx/external_128kb_upgrade/index.htm
