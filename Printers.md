---
title: Printers
layout: default
---

Unfortunately this page might be inconvenient to use from small screens such as in smartphones.

Also, note that the data in this page is about 4 years old. Some printers might be obsolete 
and there certainly are newer ones.

The table shown below shows mid-range All-In-One color printers. They all support faxing and copying.
They also are capable of costing less for ink; they all are estimated
(using an international standard for determining yield) to cost less than four cents per page for ink.
I assume that all of the most economical printers are actually quite expensive to purchase ink for.

Be sure to do some research yourself before making a purchase. At least check the Amazon reviews.
I always look at the negative reviews first; there will always be some 1-star reviews
but be skeptical of anything with more than 10% 1-star reviews.
Be sure to check the reviews for the Lexmark printers; there are enough 1-star reviews
that I debated whether to remove them from this list.
There are some other printers from all the manufacurers that I removed from here due to negative reviews.

As you can see, the Epson ET-4750 is especially economical, the ink costs about a quarter of a cent per page.
That printer actully uses ink *tanks* (EcoTanks) instead of cartridges and comes with enough ink for about 2 years.
We refill the printer from ink bottles instead of cartridges.
A bottle of Black ink costs about $20 and can print about 7,500 pages.

Some printers show a minimum number of pages to be printed monthly and I don't understand that.
For example the Brother HL-3180CDW says that the *Recommended Monthly Print Volume* is *300 to 1,500 pages*.
I assume it will not be a problem if we print fewer than the minimum number of pages per month but I am not sure.

Three of the printers from Brother are LED printers. LED printers are different.
For all other types of printers the prining mechanism, such as laser or ink jet,
must move horizontally and vertically.
LED printers however have a row of many tiny LEDs (like in LED monitors)
and the printer moves the row of LEDs in one direction only.
That means fewer moving parts. Note that LED printers actually use *toner* instead of ink
and they have drums that need to be replaced after many thousands of pages printed.

<table>
<tr>
<th>Make & Model</th>
<th>Tech</th>
<th>InkModel</th>
<th>Yield</th>
<th>IC</th>
<th>List$</th>
<th>Oth$</th>
<th>TS</th>
<th>Vol.</th>
</tr>

{% for printer in site.data.Printers.printers.printer %}
<tr>
<td>{{printer.Make}} {{printer.Model}}</td><td>{{printer.Tech}}</td><td>{{printer.InkModel}}</td>
<td>{{printer.Yield}}</td><td>{{printer.InkCost}}</td><td>{{printer.ListPrice}}</td>
<td>{{printer.OtherPrice}}</td><td>{{printer.TouchScreen}}</td><td>{{printer.Volume}}</td>
</tr>

<tr><td>&nbsp;</td>
<td colspan=8>Width: {{printer.Dimensions.Width}};
Depth: {{printer.Dimensions.Depth}};
Height: {{printer.Dimensions.Height}}
</td></tr>

{% if printer.Notes and printer.Notes != nil and printer.Notes != "" %}
<tr><td>&nbsp;</td><td colspan=8>{{printer.Notes}}</td></tr>
{% endif%}

{% endfor %}
</table>

The following provides explanations of some of the columns.

Tech
: Technology; most are either inkjet or laser; see the description above for LED

Yield
: The number of pages a Black cartridge is expected to produce (high-yield cartridges
		when available)
		
IC
: The cost of a Black ink cartridge (high-yield cartridges when available)

List$
: The price as shown in the manufacturer&#39;s page for the printer, when available

Oth$
: The price shown somewhere else, such as Amazon

TS
: TouchScreen size; a TouchScreen is like the display in smartphones; we make selections by touching the screen

Vol.
: The number of pages the printer is expected to be able to print monthly without requiring additional maintenance
