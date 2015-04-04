# Visual Display Research #


## LED Options Summary ##

| **Name/Brand** | **Type** | **Amount** | **Color** | **Peak Forward Current** | **Price** |
|:---------------|:---------|:-----------|:----------|:-------------------------|:----------|
|Kingbright|LED Bar Array|10 LEDs per array|Red, Yellow, Green|175mA|$2.14|
|Panasonic|Standard LED|1 |Red, Orange, Green|20mA|$.45|
|Lite-On|LED Bar Array|10 LEDs per array|Red, Yellow, Green|100mA|$1.40|

### LED Option 1 ###
This LED option seems the most practical for what we need. They are long enough in length that they won’t look all bunched together and they come pre-packaged in the three different colors that we want.

### LED Option 2 ###
Doing all thirty LEDs individually will not look as good as buying a pre-packaged array. That is why I believe that, while an alternative is not a good one.

### LED Option 3 ###
The LEDs that Lite-On makes are about half an inch in length. I want the user to be able to see the LEDs in each different color without them being so close together that the different strengths blend together.

## LED Driver Options Summary ##

| **Brand** | **Part Number** | **Output Current** | **Price** |
|:----------|:----------------|:-------------------|:----------|
|Texas Instruments|TLC 5917|5mA to 120mA|$1.88|
|NXP Semiconductors|4894B/4794B|10mA to 40mA|$3.51/$2.65|
|Texas Instruments|LM 3914|2mA to 30mA|$2.17|

### LED Driver Option 1 ###
The TLC 5917 is an 8bit shift register that has constant current output channels and a current range from 5mA to 120mA adjusted by an external resistor. The 5917 uses a 3.3V or 5V supply voltage. It can have a single LED on each pin or LEDs can be combined in parallel to create higher currents on a single string.

### LED Driver Option 2 ###
The HEF 4894B is a 12 bit shift register that will be used to drive the LED bars, and the HEF 4794B is a 8 bit shift register. Both will run on a supply voltage of 5V.

### LED Driver Option 3 ###
This LED Driver is just a Texas Instrument IC that takes an input voltage and lights the LEDs accordingly. From what I can tell in the data sheet it says that it can be powered for around 3V, but when hooking the LED’s up to it, the LED’s were not lighting up correctly with 3V but they did fine with 15V.

### Single LED Driver 1 Setup ###

![http://i.imgur.com/395GCtF.gif](http://i.imgur.com/395GCtF.gif)

Images taken from [HEF4894B](http://www.nxp.com/documents/data_sheet/HEF4894B.pdf) and [HEF4794B](http://www.nxp.com/documents/data_sheet/HEF4794B.pdf) datasheets.

### Single LED Driver 2 Setup ###

![http://i.imgur.com/IdyisMB.gif](http://i.imgur.com/IdyisMB.gif)

Image taken from [LM3914 datasheet](http://www.ti.com.cn/cn/lit/ds/symlink/lm3914.pdf).

## Display Screen Options Summary ##

| **Brand** | **Size** | **Operating Voltage** | **Operating Current** | **Price** |
|:----------|:---------|:----------------------|:----------------------|:----------|
|Newhaven Display|2.23 Diagonal|3V|28mA|$26.65|
|Electric Assembly|2.23 Diagonal|3.3V to 5V|15mA to 50mA|$41.87|
|Sharp|2.7 Diagonal|5V|10mA|$33.87|

### Display Screen Options 1 and 2 ###
The difference between these two options basically boils down to color and cost, therefore, choosing the most cost efficient one will be the way to go.

### Display Screen Option 3 ###
I believe that the LCD screen might look better in terms of graphics but I think that the OLED display will go with the packaging requirements better and the cost of the LCD is three times that of the OLED from option 1.

## Visual Display Research Data Sources ##

| **Type of Source** | **Title, URL, etc.** | **Using in Prototype?** |
|:-------------------|:---------------------|:------------------------|
|Web Article|[Do I Need a LED Driver](http://www.luxdrive.com/products/do-i-need-a-driver/)|No|
|Web Article|[How OLED’s Work](http://electronics.howstuffworks.com/oled5.htm)|Yes|
|Web Tutorial|[LM 3914 Tutorial](http://tronixstuff.com/2013/09/14/tutorial-lm3914-dotbar-display-driver-ic/)|Yes|
|Data Sheet|[HEF 4894B](http://www.nxp.com/documents/data_sheet/HEF4894B.pdf)|Yes|
|Data Sheet|[HEF 4794B](http://www.nxp.com/documents/data_sheet/HEF4794B.pdf)|Yes|
|Data Sheet|[LM3914 LED Bar Display Driver](http://www.ti.com.cn/cn/lit/ds/symlink/lm3914.pdf)|No|
|Data Sheet|[NTE 1508](http://pdf.datasheetcatalog.com/datasheet/nte/NTE1508.pdf)|No|
|Data Sheet|[Kingbright LED Array](http://www.kingbrightusa.com/images/catalog/SPEC/DC10SYKWA.pdf)|Yes|
|Data Sheet|[Series.pdf Lite-On](http://www.mouser.com/catalog/specsheets/lite-On-LTL-2000)|No|
|Data Sheet|[Electric Assembly](http://www.lcd-module.com/fileadmin/eng/pdf/doma/olede.pdf)|No|
|Data Sheet|[Newhaven OLED Display](http://www.newhavendisplay.com/specs/NHD-2.23-12832UCB3.pdf)|Yes|
|Data Sheet|[Sharp LCD Screen](http://www.sharpmemorylcd.com/resources/LS027B7DH01_Spec.pdf)|No|