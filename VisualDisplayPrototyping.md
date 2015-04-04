# Visual Display Prototyping #



## Block Diagram ##

![http://i.imgur.com/Squ3TYN.gif](http://i.imgur.com/Squ3TYN.gif)

## Schematic ##

![http://i.imgur.com/ETcoXNg.gif](http://i.imgur.com/ETcoXNg.gif)

## Display Logic Function Calls ##

_Represented by OLED\_Test_

**Health (update\_health(integer))**

Function Called - Update health display to integer percentage given.

**Bolt count (update\_ammo(integer))**

Function Called - Update ammo display to integer given.

**Cooldown meter (cooldown\_display(integer))**

Function Called - Update cooldown display to integer given.

**When crossbow has been loaded (load\_display(boolean))**

Function Called - Display “Crossbow Loaded” if true is read in.

**When crossbow has been hit (hit\_display(boolean))**

Function Called - Display “Crossbow Hit” if true is read in.

_Represented by LED\_Test_

**LED meter (update\_LED\_bar(integer))**

Function Called - Shift bits through the TLC 5917 and set the pins of LEDs that we want on.

## Inputs ##

| **Inputs** | **Description of Signal** | **Expected Values** |
|:-----------|:--------------------------|:--------------------|
| Power | The voltage that my block needs to operate. | 3.3V |
| SPI | SPI sends data over a single line and uses a clock line to dictate when to send the data into the specific register. When the data is ready to be sent to the OLED screen it will flag the Slave Select pin high and will send data across. | 0-3.3V |
| CLK | The clock line is being used to dictate when to send data to the TLC 5917 shift register and then when the Slave Select pin is set high it will send the data to the LEDs. | 0-3.3V |
| DATA | Data will be sent one bit at a time until a total of 5 bits have been sent across the data line. Once there have been 5 bits of data sent the Slave Select pin will be set high and the LEDs will light up accordingly. | 0-3.3V |

| **Function Name** | **Description** | **Input Parameters** | **Return Value** |
|:------------------|:----------------|:---------------------|:-----------------|
| display\_led(integer) | This function will take the integer it is given and light up the LEDs based on the integer value. | Integers 1 through 5 | None |
| display\_page(integer) | This function will display different pages based on an integer number that it is given. | Integers 6 through 9 | None |

## Outputs ##

The only outputs that I have are things that you see with your eyes, like the OLED and LED Bars.

## Test Points ##

| **Voltage Required** | **Current Draw** |
|:---------------------|:-----------------|
| 3.3V | LEDs fully on - 124 mA; OLED fully on - 69 mA |


![http://i.imgur.com/7or95TE.jpg](http://i.imgur.com/7or95TE.jpg)