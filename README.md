
# two_comparator_effect

![image](https://user-images.githubusercontent.com/12017938/99150392-944cab80-2694-11eb-8207-11434fbdeb30.png)


## lessons

this circuit is based on one described by Rob Schafer in:

- [Lesson 1 - Comparators](https://www.youtube.com/watch?v=ml8xnRFdcHY)
- [Lesson 2 - Clamping](https://www.youtube.com/watch?v=FymrxKLHy6c)

also see: [original schematic](https://www.youtube.com/watch?v=MSNrXUDO9DE) and [clamping scope example](https://www.youtube.com/watch?v=vQ15EZKisZ8)

![image](https://user-images.githubusercontent.com/12017938/99150365-610a1c80-2694-11eb-8e93-e68758f4fa7a.png)

## adaption

see this [scanlines thread](https://scanlines.xyz/t/whiteboard-schoolhouse-companion-circuits/127) for discussion on this project

video demos from this adaption:

- [2comparatorFx+recurboy](https://videos.scanlines.xyz/videos/watch/49ce42f5-12a4-4f6e-85ff-bbef453d9e1e)
- [2comparatorFx+recurboy_p2](https://videos.scanlines.xyz/videos/watch/e029e6a6-3494-4a65-8555-49e3c94d06a6)


# v0.2 bom:

## [interactive bom](https://htmlpreview.github.io/?https://github.com/langolierz/robs-whiteboard-funhouse-companion-circuits/blob/master/two_comparator_effect/bom/ibom.html)

Qty | Reference(s) | Value | tayda | mouser
--- | --- | --- | --- | ---
3 | C1, C2, C3 | 1u | A-321 | -
1 | C4 | 0.1u | A-214 | -
1 | D1 | 1n914 | A-615 | -
2 | J1, J2 | RCA | - | 490-RCJ-024
1 | J3 | Barrel_Jack | A-4118 | -
1 | Q1 | 2N3904 | A-111 | -
2 | R1, R5 | 4.7k | A-2310 | -
2 | R2, R15 | 1k | A-2200 | -
3 | R3, R4, R7 | 1.2k | A-2201 | -
1 | R6 | 680 | A-2281 | -
2 | R8, R10 | 75 | A-2193 | -
1 | R9 | 150k | A-2210 | -
1 | R11 | 47 | A-2190 | -
1 | R12 | 470 | A-2247 | -
1 | R13 | 180 | A-2278 | -
1 | R14 | 1.5k | A-2202 | -
1 | R16 | 100 | A-2245 | -
2 | RV1, RV2 | 1k | - | 652-PTV09A-4225FB102
1 | U1 | LM339 | A-022 | -
1 | U2 | LM317 | A-500 | -
1 | - | 14pin socket | A-004 | -

# build instructions:

what you need:

- soldering iron
- solder
- tin/sponge
- wire clippers
- cvbs video source
- cvbs video display
- 5v barrel plug powersupply (either to wall or to usb)

maybe useful: 

- solder braid/pump
- multi meter

## building

- note on soldering: try to remember to heat pad first (2-3seconds), then add solder, then continue to heat (1-2seconds)

- start with the resistors, taking care place the correct value resisitor in the correct footprint (if you are unsure of the value can use [this](http://resistor.cherryjourney.pt/) calculator ) , direction does not matter. lets try placing half the resistors first (up to r6) then soldering and trimming , then placing the second half

- next lets do capicitors: will need to idenitfy which is 0.1u (will say 104, while the others say 105 on it), then place them all and solder and trim.

- now lets place diodes and transistors. _take note of the direction on the diode_ - black bar on component matching black bar on footprint. also you need to read the transistors to tell which is which - they are not the same ! be careful when soldering the to92 parts the pads are very close - this is the hardest part ! (i soldered the outer legs first, trimmed these and then soldered inner)

- now lets do the ic socket -> _make sure the direction is correct!_ place in and fold two corner legs to hold in place, then solder all legs. you can place the ic in now too

- finally lets place the control parts, starting with the power jack (can use something under teh board to balance it while you solder), next place the rca jacks and pots. be generous with the solder here -> this is to strengthen the mechanical connections aswell as making electrical ones

## testing

and the circuit is done ! check for any solder bridges or unsoldered joins - use a multimeter to be sure if you have one. time to test. best to start by setting up your cvbs video source and plugging directly into the cvbs video display -> is this giving the expected image ?

next power the device (no funny smells?) , and try patching the cvbs source through the two_comparator_effect -> anything on the screen ? try adjusting the knobs - at the lower end might drop out..

