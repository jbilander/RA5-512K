# RA5-512K
A remake of the RA5-512K expansion memory for the Amiga 500 made in diptrace

This is a replica of the original RA5-512K expansion memory for the A500. Two small changes/improvements has been made to this pcb.

* Increased the pitch for the battery pins to 20 mm to accomodate for a coin cell battery holder (e.g. CR2032). Moved C2 somewhat to the right.
* Added pads for Y1 to be able to use either a surface mount MC-306 crystal or a cylinder shaped one. A crystal is needed when using an old OKI M6242B RTC chip.

<a href="images/RA5-512k_pic1.jpg">
<img src="images/RA5-512k_pic1.jpg" width="372" height="250">
</a>
<a href="images/RA5-512k_pic2.jpg">
<img src="images/RA5-512k_pic2.jpg" width="372" height="250">
</a>

Why making this replica?

* To save/reuse components from a battery damaged/corroded A501 pcb with four (256k x 4 bit) dram chips and an OKI M6242B RTC and transplant them into a new pcb.
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
TODO: Insert BOM here
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

Many different coin cell battery holders can be used for this pcb as long as they have 20 mm pin pitch. Do the soldering of the battery holder last or at least after you have populated R4 (with a resistor or a diod) as it might be in the way for the battery holder to be flush against the pcb. You may have to leave some room in between. Some battery holders have plastic standoffs/legs built into the design. See pictures below:

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

When using a non-rechargeable lithium battery it is important to stop the re-charging current to flow to the battery. This can be done by using a diod at R4 with the anode facing the positive terminal, see BOM for details of what to use here.
