# MCU Prototyping #



## Input Function List ##

| **Function Name** | **Description** | **Input Parameters** | **Return Value** |
|:------------------|:----------------|:---------------------|:-----------------|
| check\_touch | Returns data about taps or swipes from touch controller. | none | touchtype (struct) |
| im\_dead | Sends “I’m dead” packet over CANbus. | none | boolean (success) |
| receive\_packet | Check IR input for valid packets and return damage value. | none | integer |

## Input List ##

| **Input value** | **Description of Signal** | **Expected Output (over UART)** |
|:----------------|:--------------------------|:--------------------------------|
| on booting| On power up, output over UART. | Booting...initializing touch...ammo level at 30...health at 100 |
| UART: “touch tap” | Emulates tap event from check\_touch(), output is for when the firing state is “empty” | TAP EVENT; bolt loaded!; playing sound 1 |
| UART: “touch swipe 8” | Emulates swipe event of strength 8 (range: 1-9). Output only happens when firing state is “loaded”. | SWIPE EVENT; str = 8; led bar: 11111111 |
| UART: “touch tap” | Emulates tap event. Output is for when firing state is “armed”. Cooldown output is appropriately displayed per second. | TAP EVENT; firing bolt!; playing sound 2; shooting MIRP packet with strength of 8; ammo level at 29; after firing complete; not firing...cooldown at 4[…] |
| Ground external pin/button press. | Simulates IR input for IR interrupt. Takes damage. | health at 95 |
| Ground external pin until dead. |Cause health to reach 0, emulate CANbus output. | you're totally dead, dude. |


## Output Function List ##

| **Function Name** | **Description of expected outputs to function** | **Input Parameters** | **Return Value** |
|:------------------|:------------------------------------------------|:---------------------|:-----------------|
| update\_ammo | Displays the given ammo count on the screen. | integer [to max ammo](0.md) | none |
| update\_health | Displays the given amount of health on the screen. | integer [to max health](0.md) | none |
| update\_load | Displays if a bolt is loaded. | boolean | none |
| fire\_display | Displays that a bolt is firing. | boolean | none |
| cooldown\_display | Displays cooldown time in seconds. | integer [to max cooldown](0.md) | none |
| update\_led\_bar | Lights LED bar based on bits. | integer (bits) [to 8 bits](0.md) | none |
| touch\_init | Initializes touch controller. | none | none |
| play\_sound | Play a specified sound (by number). | integer [to number of sounds](0.md) | none |
| shoot\_packet | Shoot MIRP with specified strength/distance. | integer [to 9, specifying distance](1.md) | none |

### Additional Output Description ###

The output values go to other logic blocks, and therefore do not have a verifiable output for my block. The debug output for these functions (over UART) are demonstrated on the previous page.

## Signals at Test Points ##

All debug for my code block is done over UART. Statements can easily be added to output numbers or strings of data. This makes adding additional debug abilities trivial.

## Prototyping Images ##

![http://i.imgur.com/BmDUGAg.jpg](http://i.imgur.com/BmDUGAg.jpg)