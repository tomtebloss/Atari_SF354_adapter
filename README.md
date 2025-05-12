<h1 align="center">
PCB for use in an Atari SF354/314 housing.
</h1>

<h2 align="center">
Change original pcb to be able to read double sided floppy.

---

<img title="new pcb top" style="width:70%" align="center" src="images/pcb top angle.jpg">
</h2>

---

## Background  

I bought an old SF354 case with broken (dried belt) single sided floppy drive to convert to gotek. The case was for the big eject button version. Apparently there is (at least) two different version of the pcb inside. One can be used with double sided drives without modifications. And one with a lot of components on the pcb that needs modifications to work with double sided drives (the one I got). I didn't get any signal cable or power cable/brick with my SF354 so it was no meaning to modify the old pcb since I had to source a power cable for it. So I did a new PCB instead and used USB-C to power it. Only 5V. No 12V is used on this board. 

<img title="SF354 original pcb top" style="width:46%" align=top src="images/old pcb top.jpg"><img title="SF354 original pcb bottom" style="width:52%" align=top src="images/old pcb bottom.jpg">

---

## What you will need  

- 1 Adapter PCB. Order with the [gerber] file "SF354_adapter_pcb_gerber_v1.5.zip" from your favorite PCB manufactory. 
- 1 or 2 BERG 4 pin floppy power connector (or solder the wires dierectly to the pcb).
- 1 or 2 100nF (0,1uF) 0805 SMD capacitors. This can bew omitted if you want.
- 1 or 2 1uF capacitors. Either SMD (1206) or through hole (5,12mm leg pitch).
- 1 47uF electrolytic capacitor. Either SMD (size C. 6,3x7,7mm) or through hole (5mm leg pitch).
- 2 14 pin DIN connectors. Desolder from old pcb (only 1 is needed).
- 1 34 pin IDC connector. (or solder the wires directly to the pcb).
- 1 USB-C 6 pin SMD connector.
- 1 switch (SPDT) or small piece of wire if you don't use it. 
- 1 Gotek or disk drive. If Gotek is used you must remove motor on jumper. Only DS0 should be jumpered.
- 1 3D printed [bracket] for Gotek pcb. 

BOM/partlist can also be found in the [gerber] zip. There is also PDFs for some parts.

---

## How to

| Start by desoldering the two 14 pin DIN connectors from the old pcb. Solder the small capacitors on the new pcb. Choose whatever value you like. I did 1uF on the 1206 SMD ceramic capacitor and 0,1uF on the 0805 cap. Otherwise just do 1uF on the through hole if you don't like surface mount stuff. It doesn't matter really. Choose the placement closest to the connector you are going to use to power your drive. Solder in the USB-C connector. Then the 4 pin BERG connector for power. Choose a spot. Or solder wire directly to the board. You will need a female-female 4-pin power cable if you soldered in a connector on the pcb. Then solder 34 pin IDC connector and then one large 47 uF electrolytic capacitor. Choose through hole or surface mount. Either is fine. Then one or two 14 pin DIN connector. You can solder the ribbon cable directly to the pcb instead of 34 pin connector or you will have to buy a 34-pin ribbon cable for floppy otherwise. | <img title="pcb soldered - top side" style="width:46%" align=top src="images/pcb soldered top.jpg">   <img title="pcb soldered - bottom side" style="width:52%" align=top src="images/pcb soldered bottom.jpg">|
| :--- | :---: |
| I choose a switch and solder some wires and drilled, saw and filed some parts from the old gotek case. Square part goes inside of case (pic taken before I realized that I needed hole for USB connector). Small disc in the hole then large disc then switch. It will be a sandwich with the case in the middle. If you don't want a switch you have to solder a small wire between the holes that says LINK. Otherwise you will not have power for your drive. | <img title="parts for switch" style="width:65%" align=top src="images/parts for switch.jpg">   <img title="back of case" style="width:32%" align=top src="images/case with small disc.jpg"> |
| The 3D printed front panel has a hole for a 2x5mm LED. I desoldered the round one from the gotek pcb and solderd in some pinheaders instead. I then soldered some wires on a new LED. The orientation can easily be switched if it doesn't lit up. | <img title="pins on gotek for LED behind button" style="width:62%" align=top src="images/gotek pins for led.jpg">   <img title="2x5mm LED with wires and heat shrink tube" style="width:36%" align=top src="images/led 2x5mm.jpg"> |
| Assemble everything. Fasten with screw. I also used a rotary encoder and a buzzer on my gotek. You can use whatever mod you like on yours. Check flashfloppy [hardware mods]. | <img title="all mounted" style="width:100%" src="images/all mounted.jpg"> |
| <img title="Assembled front side" style="width:58%" align=right src="images/finished front.jpg"> | <img title="Assembled back side" style="width:100%" src="images/finished back.jpg"> |

---

## Testing

I tested this with a Mega ST 1 upgraded to 4Mb and with a TSENG ET4000AX graphics card. I also used 256Kb roms (EmuTOS v1.3 and TOS v2.06). I used two Goteks in the picture below but I also tested with two real floppy disk drives. But it should work with any double sided drive and system I hope.

<img title="screenshot" width="500rem" src="images/screenshot with A and B.jpg">
<img title="testsystem" width="500rem" src="images/testsystem.jpg">

---

PCB made by Daniel Guldkrans aka DoG in Eagle April 2025.






[gerber]: gerber/SF354_adapter_pcb_gerber_v1.5.zip
[bracket]: https://www.thingiverse.com/thing:6960806
[hardware mods]: https://github.com/keirf/flashfloppy/wiki/Hardware-Mods
