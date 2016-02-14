# cmoy-bdx headphone amplifier

Information on Chu Moy headphone amplifier, in bdx style, modified by me, Kenji Rikitake.

## What is Chu Moy headphone amplifier?

The Chu Moy amplifier is made of one-chip two-circuit OpAmp, using each circuit for one of the stereo channels. Unfortunately the original article in headwize.com has been gone (in fact the domain is gone), but still some good references remain online:

* [How to Build the CMoy Pocket Amplifier](http://tangentsoft.net/audio/cmoy/)
* [Virtual Ground Circuits](http://tangentsoft.net/elec/vgrounds.html)

## Undocumented latest mods

* Replacing OPA2134PA to OPA2604AP caused the chip to self-oscillate. So I removed 47 ohm resistors (R5) and short-circuited them (= zero ohm) between the output terminals of OpAmps and the feedback resistor (R4).  I also add new metal-film resistors of 110 ohm between the output feedback points and the headphone terminals, to reduce effects of reactance connected at the headphone terminals.  This effectively prevented further self-oscillation for the following chips: OPA2134PA, OPA2604AP, NJM4580DD, NJM2043D, and TLE2072.

* The output jack is now 1/4" or 6.5mm diameter jack. No electrical difference, but for compatibility with my headphones.

* C1 (2.2uF between VR and OPamp input) can be removed and short-circuited if the input is guaranteed to be DC voltage free. (In my case I attach a TI PCM2704 USB DAC board to the amplifier with dedicated 2.2uF mylar caps. See [Akizuki Denshi's PCM2704 board kit](http://akizukidenshi.com/catalog/g/gK-05369/) (article in ja\_JP).

* Choice of input volume: Panasonic's EVJ-Y10F03A14 (available as [Digi-Key part number P2G1103-ND](http://www.digikey.com/product-detail/en/EVJ-Y10F03A14/P2G1103-ND/243525) ) is a very good choice as a 10kohm x 2 audio curve potentiometer. Do not put too much force on each of the connection leads because they are thin and get easily bent.

* The power switch is removed.

* The power supply has DC 18V regulated voltage.

* BUF634 Pin 1 is connected to Pin 4, for using it in the wide-band mode.

* Two electrolytic capacitors of 470uF 25V are added between V+/V- and BUF634 output, to stabilize the virtual ground.
