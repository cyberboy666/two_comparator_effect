# two_comparator_effect
### analog video posterisation effect - adapted from a rob schafer design

![image](https://user-images.githubusercontent.com/12017938/150422990-b99b74ae-0009-4dd7-946b-c375e2f60bf9.png)

- this circuit is distributed by __UNDERSCORES__ - _an open video hardware label_ : it is available to purchase - as a pcb, kit or assembled unit - at [underscores.shop](https://underscores.shop/two_comparator_effect/)
- the schematic for the circuit can be found [here](/hardware/schematic.pdf)
- the pcb gerber files for the lastest version can be found [here](/hardware/gerber_latest.zip)
- consider [donating](https://liberapay.com/underscores/) to the underscores project to help us continue creating for the commons

## demo video

[![image](https://user-images.githubusercontent.com/12017938/153121223-3dfda130-a8e7-405d-b214-ceade0454927.png)](https://videos.scanlines.xyz/w/t1Ht54aVoeiCa2ZGb4LRMV)


## background

<details>
<summary>background</summary>

Rob Schafer designed the original version of this circuit in his excellent [whiteboard schoolhouse](https://www.youtube.com/watch?v=9HMj0sfPa0w&list=PLoNU5z_Oqfgj1xfSBMg6XaIhAX2ftyfkN) youtube series.

It was updated and adapted to pcb by cyberboy666 as open-source hardware with help from the [scanlines community](https://scanlines.xyz/t/whiteboard-schoolhouse-companion-circuits/127/23) – this version debuted as a mail-in soldering workshop for [VIDICON_2020](https://vidicon.org/)

<img src="https://user-images.githubusercontent.com/12017938/150426512-9717722a-03d2-48e7-8298-26b80e0a6d3f.png" width="500">

<img src="https://user-images.githubusercontent.com/12017938/150426587-113872c9-3679-49a4-890b-48b5126a33b2.png" width="500">

<img src="https://user-images.githubusercontent.com/12017938/150426600-25b713fe-6b22-4d85-9e1d-3f3544dda357.png" width="500">

robs original circuit, the schematic and effect shown here 

</details>
  
# documentation

this project is fully _open-source hardware_ - all the files required to build it are included in this repo for free. if you have the time and/or skill you can contribute back by collaborating on / testing new designs, improving these docs, making demo videos/other creative content etc. you can also support the project financially by [donating](https://liberapay.com/underscores/) directing, or purchasing through the [web shop](https://underscores.shop).

depending on whether you are going fully diy or buying an assembled and tested unit, some of the following guides will be relavent to you. the flow would be:

## ordering parts

<details><summary><b>parts sourcing guide (w/ notes on pcb fabracation )</b> - start here if you are building fully from scatch or have purchased a pcb</summary>
  

i try to source all the parts i can from either:
- [tayda](https://www.taydaelectronics.com/) ; cheaper for common parts like resistors etc, also good for mechanical parts like switches and buttons
- [mouser](https://www.mouser.de/) ; has lots more options, speciality video ic's, can sometimes cost more (free shipping on orders over 50euros)
- other ; ocationally there will be parts which will need to be sourced elsewhere - usaully either aliexpress, ebay or amazon etc...

take a look at the [full_bom](/hardware/bom/full_bom.csv) for this project to see where i am sourcing each part from

## import into tayda

- go to the [tayda quick order](https://www.taydaelectronics.com/quick-order/) and in bottom corner choose _add from file_
- select the file [tayda_bom.csv](../hardware/bom/tayda_bom.csv) in the BOM folder (you will have to download it first or clone this repo)
- after importing select _add to cart_
- __NOTE:__ the minimum value for resistors is 10, so you may need to modify these values to add to cart (or if they are already modified here you will need to see the  full_bom for actual part QTY) 

- OPTIONAL: it is a good idea to add some dip-ic sockets and 2.54pin headers/sockets to your tayda order if you dont have them around already
  
## import into mouser

- go to [mouser bom tool](https://nz.mouser.com/Bom/) and click _upload spreadsheet_
- select the file [mouser_bom.csv](../hardware/bom/mouser_bom.csv) in this folder (you will have to download it first or clone this repo), then _upload my spreadsheet_ and _next_
- ensure that __Mouser Part Number__ is selected in the dropdown above the first row, then _next_, _process_
- if everything looks correct can now put _add to basket_

# ordering pcbs

you can support this project by buying individual pcbs from the [shop](https://underscores.shop). if you would rather have pcbs fabricated from gerbers directly the file you need is [here](/hardware/gerber_latest.zip)

- i get my pcbs fabricated from [jlcpcb](https://cart.jlcpcb.com/quote) - 5 is the minumum order per design
- upload the zip file with the `add gerber file` button
- the default settings are mostly fine - set the __PCB Qty__ and __PCB Color__ settings (you can check that the file looks correct with pcb veiwer)
- it may be best to combine orders with other pcbs you want to have fab'd since the shipping can cost more than the items - also orginising group buys is a good way to distribute the extra pcbs /costs 
  
i often use jlcpcb because they are reliable, cheap and give you an option of colours. remember though that the cheapest Chinese fab houses are not always the most ethical or environmently friendly - if you can afford it consider supporting local companies. 

  </details>
  
## assembly guide
  
<details><summary><b>assembly guide</b> - start here if you have purchased a diy kit</summary>

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
  
</details>

## operating guide
  
<details><summary><b>operating guide</b> - start here if you have purchased an assembled unit</summary>

  ![image](https://user-images.githubusercontent.com/12017938/152089017-3b2bcf51-c725-48ac-adf9-8fc9530a3fab.png)

- To set up using the circuit plug an active video source into composite video input and a display into composite video output (flipping the bypass switch should show the raw video source passing through the circuit to the display)

- Next plug in a 5v center-positive power supply into the 2.1mm barrel jack connector – I like to use a usb wall charger for this

- switch the bypass again to activate the circuit - Adjusting the level knobs should change the resulting image – the thresholds control which brightness levels result in white black or gray regions.

- Depending on your display setting either or both knobs fully counter-clockwise can result in glitchy effects, colour bleeds and sync drops

</details>

### more info

<details><summary><b>how the circuit works</b></summary>
  
Watch the youtube videos [Lesson 1 – Comparators](https://www.youtube.com/watch?v=ml8xnRFdcHY) and [Lesson 2 – Clamping](https://www.youtube.com/watch?v=FymrxKLHy6c) by Rob Schafer for full explanation. See full schematics on the project page.
  
This circuit works by using multiple stages of an LM339 - Quad Differential Comparator ic. 

<img src="https://user-images.githubusercontent.com/12017938/150246024-eef596d9-f7bf-47e8-9f3c-75253b6eb628.png" width="300">
  
A comparator stage compares the two voltages on its input (plus and minus) and outputs high if plus > minus, low if plus < minus. Since we power the ic with +5v, in this case high is an output of +5v and low is an output of 0v
                                                                                                                                 
comparator plus input is connected to the analog video signal (where higher voltage corresponds to a brighter image)

<img src="https://user-images.githubusercontent.com/12017938/150246234-c94c753b-e754-46f7-baa9-8e1b3718dbaf.png" width="500">
  
The minus input is connected to a reference voltage which can be set by turning a potentiometer. varying the pot adjusts the resistance in this voltage divider configuration which in turn varies the voltage supplied as reference
                                                                                                                                 

The result of this effect is an image that is all white for regions of the original image above a given brightness threshold level, and all black for the regions below this level. Changing this threshold changes which parts of the image are set to black vs white.

Here is a scoped example of an original signal (top) with threshold and the resulting signal (bottom)

<img src="https://user-images.githubusercontent.com/12017938/150246284-0d3b6568-5050-4080-86ba-3a94f5811e34.png" width="500" >
                                                                                                                                 
Before reaching the comparators, the incoming video signal needs to be SOFT CLAMPED – this is done using a capacitor, diode and a 1.25v rail that was obtained with a LM317 voltage regulator.

<img src="https://user-images.githubusercontent.com/12017938/150246604-b2fafc8f-fde6-4ab2-b7e4-a7b3cf384891.png" width="500">

A composite video signal tends to squash up when the image is bright and spread out when it is darker.

For the comparator reference voltages to be consistence we need to correct for this behavior by clamping the signal to a fixed voltage level
                                                                                                                                 
<img src="https://user-images.githubusercontent.com/12017938/150246396-91f87d61-a8e7-408e-a68e-be99e1eb76b3.png" width="500">

A third comparator stage with a fixed reference voltage is used to ‘pick off’ the sync pulse of the original signal.

The output from these three comparator stages are scaled and combined to create a new composite video signal with the desired effect
                                                                                                                                 
<img src="https://user-images.githubusercontent.com/12017938/150246738-2d2b730e-b697-4c1f-817a-87f1955b7855.png" width="500" >

Composite video encodes color as a sub-carrier frequency over the signal.

This circuit is designed for use with gray-scale video input where no sub-carrier is present, although it does still work with color input – usually ignoring the _sub-carrier_, although occasionally there are some artifacts generated by this. This is more common with NTSC than with PAL

glitch artifacts are also created when the comparator thresholds are set below the _black-level_ of the video signal, causing the signal to lose sync. 
                                                                                                                             
</details>

<details><summary><b>contributing guide</b></summary>
  
if you would like to contribute back to these projects in some way but dont know how the best thing (for now) would be to reach out to me directly ( tim@cyberboy666.com or @cyberboy666 on scanlines forum) - i will be happy to help
  
</details>


## credits & more info


This circuit is distributed through UNDERSCORES – open video hardware label – visit [underscores.shop](https://underscores.shop) for more info

The pcb was designed using KICAD , the booklet was created in LibreOffice Draw

Everything from gerbers, cad files, panels and documentation is freely available online and distributed under CC-BY-SA / open-source licenses – help us contribute to the commons !

Ask any questions or start discussions related to this project on the [scanlines.xyz](https://scanlines.xyz) forum – an online community space dedicated to diy av / electronic media art

You can contact me directly at tim (at) cyberboy666 (dot) com 
Please get in touch if you are interested in hosting a workshop !

<img src="https://user-images.githubusercontent.com/12017938/150428011-7b77f517-786f-410d-8d07-c8bbc48bab62.png">

Thanks to Rob Schafer for sharing your designs and knowledge. to Bastien Lavaud for circuit advice, always. To Guergana Tzatchkova for booklet design inspiration. To Ben Caldwell for project advice. To everyone who has or will contribute ♥♥♥

