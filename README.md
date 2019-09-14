# RA5-512K
A remake of the RA5-512K expansion memory for the Amiga 500 made in diptrace

This is a replica of the original RA5-512K expansion memory for the A500. Two small changes/improvements has been made to this pcb.

* Increased the pitch for the battery pins to 20 mm to accomodate for a coin cell battery holder (e.g. CR2032). Moved C2 somewhat to the right.
* Added pads for Y1 to be able to use either a surface mount MC-306 crystal or a cylinder shaped one. A clock crystal is needed when using an old OKI M6242B RTC chip.

<a href="images/RA5-512k_pic1.jpg">
<img src="images/RA5-512k_pic1.jpg" width="372" height="250">
</a>
<a href="images/RA5-512k_pic2.jpg">
<img src="images/RA5-512k_pic2.jpg" width="372" height="250">
</a>

Why making this replica?

* To save/reuse components from a battery damaged/corroded A501 pcb with four (256k x 4 bit) dram chips and an OKI M6242B RTC and transplant them into a new pcb. That is if the pcb is damaged beyond rescuing, otherwise look <a href="https://github.com/jbilander/HowTos/wiki/How-to-fix-and-use-a-3V-lithium-coin-cell-battery-with-an-old-A501-Amiga-expansion-memory">here</a>
* Preserving a bit of history.
* For testing out diptrace.


Sending off gerbers to the Aisler boardhouse and received three good looking boards.
* https://aisler.net/p/OHZYVCCU

***

<a href="images/RA5-512k_pic3.jpg">
<img src="images/RA5-512k_pic3.jpg" width="202" height="151">
</a>

This is how the end result looks like after populating this board:

<a href="images/RA5-512k_pic4.jpg">
<img src="images/RA5-512k_pic4.jpg" width="202" height="151">
</a>

***
BOM RA5-512

* BAT: Any cheap Battery Holder for CR2032 (Two pin 20 mm pitch) or one 3.6V NiCd rechargeable barrel battery (two pin 20 mm pitch).

* J1: 1 x 56pin (2×28) 2.54mm double row right-angle header (or 2x40pin and cut it with a hacksaw)

* U1-U4: 4 pcs MCM514256AP70 Integrated Circuit DIP-20 DRAM, 256Kx4, 70ns, CMOS or equivalent e.g. MB81C4256A-70P
* 4 pcs DIP-20 socket (optional)

* U5: OKI M6242B RTC or RTC 62421A
* 1 pcs DIP-18 socket (optional)
* Y1: Clock Crystal 32.768kHz, cylinder shaped Ø2x6mm or surface mounted MC-306 32.768kHz clock crystal
,populate only if using chip OKI M6242B or similar chip without built-in crystal

Metal Film Through Hole Resistors
* R1: 10k Ohm 
* R2: 470 Ohm
* R3: 47 Ohm
* R4: 470 Ohm or with non-rechargeable Lithium Coin cell replace with diod 1N4148 / 1N914 - Small Signal Switching Diode, DO-35 glass, 100 V, Anode connected to the battery positive terminal.

* RP1, RP2, RP3: 8-pin isolated Fixed Resistor Network. A single in line (SIL) resistor package with 4 individual, 47 ohm resistors.
e.g. 4608X-102-470LF - Fixed Resistor Network 47 Ohm ± 2 %, Bourns

* D1, D2: 1N4148 or 1N914 - Small Signal Switching Through Hole Diode, DO-35 glass, 100 V

* C1, C10, C11, C12: Radial Electrolytic Capacitor 22uF 16V (or higher V)
* C2, C5, C6, C7, C8, C9: 104 ( 0.1uF = 100nF ) Ceramic Decoupling Capacitor
* C3, C4: Ceramic Disc Capacitor 20pF 50V

* JP1: 1 x 2 pin 2.54mm header 

JP1 is for enabling/disabling the EXRAM line.
***

This is how the original battery damaged/corroded board looked like. The NiCd battery had leaked and the Cadmium has eaten a large chunk of the copper. I desoldered all the components to reveal all the traces for reverse engineering to take place.

<a href="images/RA5-512k_pic5.jpg">
<img src="images/RA5-512k_pic5.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic6.jpg">
<img src="images/RA5-512k_pic6.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic7.jpg">
<img src="images/RA5-512k_pic7.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic8.jpg">
<img src="images/RA5-512k_pic8.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic9.jpg">
<img src="images/RA5-512k_pic9.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic10.jpg">
<img src="images/RA5-512k_pic10.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic11.jpg">
<img src="images/RA5-512k_pic11.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic12.jpg">
<img src="images/RA5-512k_pic12.jpg" width="202" height="151">
</a>

***

Choosing a suitable battery holder:

Many different coin cell battery holders can be used for this pcb as long as they have 20 mm pin pitch. Do the soldering of the battery holder as a last step or at least after you have populated R4 (with a resistor or a diod) as it might be in the way for the battery holder to be flush against the pcb. You may have to leave some room in between. Some battery holders have plastic standoffs/legs built into the design. See pictures below:

<a href="images/RA5-512k_pic13.jpg">
<img src="images/RA5-512k_pic13.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic14.jpg">
<img src="images/RA5-512k_pic14.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic15.jpg">
<img src="images/RA5-512k_pic15.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic16.jpg">
<img src="images/RA5-512k_pic16.jpg" width="202" height="151">
</a>

***

When using a non-rechargeable lithium battery it is important to stop the re-charging current to flow to the battery. This can be done by using a diod at R4 with the anode facing the positive terminal, see picture below and BOM for details of what to use here.

<a href="images/RA5-512k_pic17.jpg">
<img src="images/RA5-512k_pic17.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic18.jpg">
<img src="images/RA5-512k_pic18.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic19.jpg">
<img src="images/RA5-512k_pic19.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic20.jpg">
<img src="images/RA5-512k_pic20.jpg" width="202" height="151">
</a>

***

Populating the RTC socket with a 62421A chip which has a built-in crystal we don't populate Y1. Adding the dram chips and och 3V lithium coin cell (CR2032) we can measure if we got any voltage on the RTC. And we sure do, the small voltage drop is normal due to the use of the diod.

<a href="images/RA5-512k_pic21.jpg">
<img src="images/RA5-512k_pic21.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic22.jpg">
<img src="images/RA5-512k_pic22.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic23.jpg">
<img src="images/RA5-512k_pic23.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic24.jpg">
<img src="images/RA5-512k_pic24.jpg" width="202" height="151">
</a>

***

Time to try this one in a real Amiga 500 now, this A500 motherboard is a Rev.6A with the JP2 and JP7A modded so if this expansion memory works it will show up as chip ram...and voila!, we can see we got 1 MB in total. Let's run some tests and check the RTC voltage level with the machine on. We can see the chip ram works, the RTC ticks and the voltage level is nice at just above 5V.

<a href="images/RA5-512k_pic25.jpg">
<img src="images/RA5-512k_pic25.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic26.jpg">
<img src="images/RA5-512k_pic26.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic27.jpg">
<img src="images/RA5-512k_pic27.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic28.jpg">
<img src="images/RA5-512k_pic28.jpg" width="202" height="151">
</a>

***

Now let's try with the OKI M6242B RTC. First without adding a crystal to Y1 :) As expected the clock doesn't tick.

<a href="images/RA5-512k_pic29.jpg">
<img src="images/RA5-512k_pic29.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic30.jpg">
<img src="images/RA5-512k_pic30.jpg" width="202" height="151">
</a>

So, let's solder on a crystal and try again. Now it ticks along...

<a href="images/RA5-512k_pic31.jpg">
<img src="images/RA5-512k_pic31.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic32.jpg">
<img src="images/RA5-512k_pic32.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic33.jpg">
<img src="images/RA5-512k_pic33.jpg" width="202" height="151">
</a>
<a href="images/RA5-512k_pic34.jpg">
<img src="images/RA5-512k_pic34.jpg" width="202" height="151">
</a>

***

After running the memtest for several hours without any problems I consider this expansion card now working as it should.

<a href="images/RA5-512k_pic35.jpg">
<img src="images/RA5-512k_pic35.jpg" width="202" height="151">
</a>

***

The final result once again:

<a href="images/RA5-512k_pic36.jpg">
<img src="images/RA5-512k_pic36.jpg" width="404" height="302">
</a>
