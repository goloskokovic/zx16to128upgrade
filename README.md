# 128k RAM expansion for ZX48k
Upgrade ZX Spectrum 48k with 128k of RAM and play all the games you couldn't play before. The sound will stay as before, but you can always make an AY interface to sound as ZX Spectrum 128k.

https://www.pcbway.com/project/shareproject/W219199ASS53_AY_kempston_gerber.html

In order to make the RAM expansion work, a small modification to your ZX Spectrum 48k is required to disable 32k upper RAM.
For Issue 2/3/4 connect pin 5 on IC23 (74LS32) to pin 14 (+5V). For Issue 5/6 connect pin 35 on IC27 (ZX8401) to pin 40 (+5V).

https://spectrumcomputing.co.uk/forums/viewtopic.php?t=2616

![image](/Images/CAS.png)

With this mod without the RAM expansion, your ZX Spectrum 48k will work as ZX Spectrum 16k. 



![image](/Images/brd.png)

![image](/Images/rev2.jpg)


Original page: https://velesoft.speccy.cz/zx/external_128kb_upgrade/index.htm
