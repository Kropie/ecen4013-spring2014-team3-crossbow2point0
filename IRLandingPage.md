# IR Block #



Hardware for the IR block was designed by Anthony Gaskill.  Software was completed by Colt Wilkens.  There was no formal research and prototyping phase for this block.

## IR Block Diagram ##

![http://i.imgur.com/nqzKyd9.gif](http://i.imgur.com/nqzKyd9.gif)

## IR Send ##

The crossbow will have one IR LED which is used to emit different numbers of damage packets based on input from the capacitive touch interface.  When the user swipes along the capacitive touch board, the swipe distance corresponds with a different number of packets being sent; the longer the swipe, the more packets that are emitted when the crossbow is fired.

#### IR Send Schematic ####

![http://i.imgur.com/gYxcaeo.png](http://i.imgur.com/gYxcaeo.png)

#### IR Send Prototyping ####

![http://i.imgur.com/S0tFFsV.jpg](http://i.imgur.com/S0tFFsV.jpg)

## IR Receive ##

The IR receiver is simple, only requiring three pins: power, ground, and output.  Power is connected to 5 volts and output is connected to the MCU.  An interrupt is triggered at the MCU when a signal is received.  The MCU then determines if the signal is a valid packet for the M.A.G.E. system.

#### IR Receive Schematic ####

![http://i.imgur.com/BXf9PX4.png](http://i.imgur.com/BXf9PX4.png)


#### IR Receive Prototyping ####

![http://i.imgur.com/jdOndmX.jpg](http://i.imgur.com/jdOndmX.jpg)

## Abandoned IR Send Concept ##

The original circuit was designed with an active-high demultiplexer, which made all of the transistors “normal on,” rendering the circuit useless.  This mistake was made due to misreading the datasheet and could have been easily avoided.  It was then decided to use a shift register, requiring fewer MCU IO pins.  After the failure of the variable current circuitry, a MOSFET IC was used to create an IR transmission circuit with a single power setting.

#### Abandoned IR Send Prototyping ####

![http://i.imgur.com/GqjJCA0.jpg](http://i.imgur.com/GqjJCA0.jpg)