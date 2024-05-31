<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

It is a simple voltage-controlled oscillator, based on ring oscillator with transmission gate <br/>
to control current flow to the gates. <br/>
The inverter gates are wired in parallel with a capacitor, to ensure that it remains linear when charging <br/>
This should directly affect the gate voltage when charging. ensuring that it stays in linear region means that <br/>
changes in resistance will proportionally change the charging time of the capacitor (e.g. 2x increase in <br/>
resistance will result in 2x longer charging time, thus halving the frequency of the oscillator), although this <br/>
concept will be limited by the linearity of the mosfets in the transmission gates. 
<br/>
<br/>
it is currently unknown why this works, since the the concept is very similar to a mosfet with really big <br/>
gate capacitance. Might be something with the current draw when charging, using cap vs not using cap?

## How to test

To test the oscillator, 2 power supply as the oscillator input is required <br/>
the VCON+ and VCON- can be thought as a differential input. to get maximum frequency, <br/>
connect 1.8V to VCON+ and 0V to VCON-. The frequency should be between 6-7 MHz.

## External hardware

List external hardware used in your project (e.g. PMOD, LED display, etc), if any
