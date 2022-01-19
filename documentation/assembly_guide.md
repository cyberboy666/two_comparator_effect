# assembly guide

## interactive BOM for build guiding

follow this link to view the [interactive BOM](https://htmlpreview.github.io/?https://github.com/cyberboy666/two_comparator_effect/blob/main/hardware/bom/ibom.html)

## general solder advice

- remember to heat pad first (2-3seconds), then add solder, then continue to heat (1-2seconds)

- Checkout the web-comic [soldering is easy](https://mightyohm.com/files/soldercomic/FullSolderComic_EN.pdf) for more soldering advice

## general order of assembly

- in general while assembling i start placing resistors and capacitors first. placing 5 - 10 components at a time and then flipping the board to solder them and trim the legs etc.
- next i would do diodes, transistors and ic's - taking care that these are placed in the right direction (using a ic socket can be useful)
- finally i place the interface parts - rca jacks, power jack, pots and switches - make sure these have lots of solder on for structural stablity

## slightly more specific assembly advice

- start with the resistors, taking care place the correct value in the correct footprint (if you are unsure of the value can use an online resistor calculator ) , direction does not matter. Place a few resistors in (as many as you are comfortable with) then solder and trim legs

- next lets do capacitors: 0.1u will say 104, while 1uf will say 105 on them - place them all and solder and trim.

- now lets place diodes and transistors. take note of the direction on the diode - black bar on component matching black bar on footprint. Transistor values are printed on thembe sure not to mix them up ! be careful when soldering the to92 parts the pads are very close - this is the hardest part - i soldered the outer legs first, trimmed these and then soldered inner.

- now lets do the ic/socket -> make sure the direction is correct! place in and fold two corner pins to hold in place, then solder all pins. you can place the ic in now too.

- finally lets place the control parts, starting with the power jack (can use something under the board to balance it while you solder), next place the rca jacks and pots. be generous with the solder here -> this is to strengthen the mechanical connections as well as making electrical ones
