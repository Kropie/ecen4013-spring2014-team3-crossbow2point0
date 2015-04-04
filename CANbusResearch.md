# CANbus Research #



## Typical CANbus Network ##

Our microcontroller has a built in CAN system, but requires an external transceiver.

![http://i.imgur.com/Cv7ujx7.gif](http://i.imgur.com/Cv7ujx7.gif)

Image taken from [ECAN datasheet](http://ww1.microchip.com/downloads/en/DeviceDoc/70226C.pdf).

## CAN Tranceiver Options Summary ##

| **Part Number** | **Voltage** | **Baud rate** | **Price** |
|:----------------|:------------|:--------------|:----------|
|MCP2551|4.5-5.5V|1 Mbit/s|$1.12|
|SN65HVD231DR|3.3V|1 Mbit/s|$2.29|

## CAN Transceiver Option 1 ##

The MCP2551 is a common and fairly straightforward CAN Transceiver. The voltage required lies within the range that our power source will be able to deliver, and the current requirement in high speed mode is less than 610 µA. The chip is also fairly small, which will help in packaging since our project has to be arm mounted, and it is on the cheaper end of CAN transceivers. Knowing that previous teams have had success with this chip was enough to put it as our number one option.

![http://i.imgur.com/8Cig7YA.gif](http://i.imgur.com/8Cig7YA.gif)

Image taken from [CAN Tranceiver datasheet](http://ww1.microchip.com/downloads/en/DeviceDoc/21667d.pdf).

## CAN Transceiver Option 2 ##

Our second option, the SN65HVD231DR, is similar to the MCP2551 in that it is a small chip as well as relatively cheap. CAN Transceivers are all very similar and do a similar job, so there is not very much distinctively different.

## CANbus Research Data Sources ##

| **Type of Datasource** | **Title, URL, etc.** | **Using in Prototype?**|
|:-----------------------|:---------------------|:-----------------------|
|Online Article|http://www.esacademy.com/en/library/technical-articles-and-documents/can-and-canopen/selecting-a-can-controller.html|No|
|Online Article|http://esd.cs.ucr.edu/webres/can20.pdf|Yes|
|PIC24 Datasheet|http://ww1.microchip.com/downloads/en/DeviceDoc/70293G.pdf|Yes|
|ECAN Datasheet|http://ww1.microchip.com/downloads/en/DeviceDoc/70226C.pdf|Yes|
|Option 2 Datasheet|http://ww1.microchip.com/downloads/en/DeviceDoc/21667d.pdf|No|
|Option 3 Datasheet|http://www.ti.com/lit/ds/slos346k/slos346k.pdf|No|