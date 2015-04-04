# Audio Research #


## Audio Driver Options ##

### Plan A: ISD1932 Recording Chip ###
The ISD1932 records sounds as a messages and it outputs them by having the sound to go through the amplifier and then through an external speaker. It is able to store up to 64 seconds depending on an oscillator resistor and sample frequency. The reason of choosing this chip as a plan A because it has a built in memory storage and an amplifier. The method of communicating with the microcontroller is by addressing bits through I/Os and that requires less complexity when writing the code. Also, the chip costs less than the chips used in plan B.

Available at !Digikey

|ISD1932|$6.28|
|:------|:----|

![http://i.imgur.com/PXytulI.gif](http://i.imgur.com/PXytulI.gif)

![http://i.imgur.com/w1fomQ1.gif](http://i.imgur.com/w1fomQ1.gif)

Images taken from [ISD1932 datasheet](http://www.nuvoton.com/hq/enu/ProductAndSales/ProductLines/AudioApplicationIC/ISDVoiceIC/ISDChipCorder/Documents/ISD1900.pdf).

### Plan B: SD card, DAC chip, Audio Amplifier chip ###
This option requires the usage of two chips in order to carry the sound to the speaker. Basically the sound files will be stored in the SD card as WAV format. The SD card will send the Data to DAC (Digital to Analog Converter) and then sound will be amplified using an amplifier to be played through the speaker.  This option is a secondary option as it is more expensive and it involves complex coding to get all chips working.

Available at Mouser

|Micro SD card|SD card Case|DAC chip|Op-amp LM386|
|:------------|:-----------|:-------|:-----------|
|$6.74|$ |$3.33|0.33|

## Speakers ##

The following are options for speakers.

### Plan A: Round PUI Speaker (8ohm, 1Watt, 80dB) ###
The speaker is manufactured by PUI and it has a dimensions of 28mm (1.102 inch) diameter and 5.2mm (0.204 inch). According to the ISD1932 datasheet, The ISD1932 chip requires an impedance of 8 ohm and a maximum power of 670mW delivered to the speaker. Therefore, choosing this kind of speaker will be compatible with the ISD1932.

Available at DigiKey

|Round PUI Speaker (8ohm, 1Watt)|$3.85|
|:------------------------------|:----|

### Plan B: Rectangle PUI Speaker (8ohm, 2Watt, 84dB) ###

The second option on the audio drive did not mention a specific maximum power as the power may be determined by the user. Therefore, 8 ohm speaker is chosen as both options A and B don’t conflict. Also, it has a 2 watt power output with a maximum 4 watt. I choose this speaker because in case we need more power output and a different shape on design. Also the speaker became a secondary option as it is more expensive.

Available at DigiKey

|Rectangle PUI Speaker (8ohm, 1Watt)|$6.13|
|:----------------------------------|:----|

## Shift Register ##

The following are options for speakers.

### Plan A: 8bit shift register ###
This is a serial input-parallel output device that will be the connection between the MCU and the ISD1932. The ISD1932 requires 8 I/0s for memory access. Due to the limitation of the number of PIC’s I/0s, this device will be needed. Also, It uses 50mA.

Available at DigiKey

|Shift-Register|$0.12|
|:-------------|:----|

### Plan B: 8Bit Shift Register ###
This shift register may be the same as the one in the first place. However, this chip consume more current as a result it became a secondary option. In addition, It uses 75 mA.

Available at DigiKey

|Shift-Register|$0.13|
|:-------------|:----|

## MultiSim Schematic ##

_Insert MultiSim Schematic of ISD1932 and Speaker_

## Audio Research Data Sources ##

|Type of datasource|Title, URL, etc.|Using in Protoype?|
|:-----------------|:---------------|:-----------------|
|ISD1932|http://www.nuvoton.com/hq/enu/ProductAndSales/ProductLines/AudioApplicationIC/ISDVoiceIC/ISDChipCorder/Documents/ISD1900.pdf|Yes|
|Micro SD card|http://www.mouser.com/catalog/specsheets/microSDSPEC.pdf|NO|
|DAC|http://www.ti.com/lit/ds/slas231b/slas231b.pdf|NO|
|Amplifier|http://www.ti.com/lit/ds/symlink/lm386.pdf|No|
|Round Speaker|http://www.puiaudio.com/pdf/AS02808MR-R.pdf|Yes|
|Rectangular speaker|http://www.puiaudio.com/pdf/AS04008PS-4W-WR-R.pdf|NO|
|Shift-Register|http://www.ti.com/lit/ds/symlink/sn74hc164.pdf|Yes|
|Shift-register 2nd|http://www.fairchildsemi.com/ds/MM/MM74HC164.pdf|No|
|3.5mm phone jack|http://www.tensility.com/pdffiles/CA-2205.pdf|Yes|