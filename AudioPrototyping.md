# Audio Block Prototyping #



## Block Diagram ##

![http://i.imgur.com/sAhNhZP.gif](http://i.imgur.com/sAhNhZP.gif)

## Schematic ##

![http://i.imgur.com/Qc78Ndb.gif](http://i.imgur.com/Qc78Ndb.gif)

## Code Flowchart ##

![http://i.imgur.com/NXARGQu.gif](http://i.imgur.com/NXARGQu.gif)

## Function List ##

Delay function: it delays the execution of code for some time.
delay(); - no return

Playback function: it plays the desired song by sending the right amount of data serially to the shift register.
play\_song(int song); - no return

Clear function: it clears all the bits from the shift register to set it up for sending data in or wipe them out.
clear\_all(); - no return

## Software and Hardware Input ##

| **Input Name** | **Description of Signal** | **Expected Range** |
|:---------------|:--------------------------|:-------------------|
| Power | Needed operation voltage | 2.4-3.3V |
| Data | 8 bit Serial data send to the shift register containing which file to play | 2.4-3.3V |
| Clock | It’s a signal from which the shift register knows when to receive data | 2.4-3.3V |
| Clear | It’s a signal that clears any residual data in the shift register |

| **Function Name** | **Description** | **Input Parameters** | **Return Value** |
|:------------------|:----------------|:---------------------|:-----------------|
| Clear\_all | It clears all data in the shift register | None | None |
| Play\_song | It calls a function to play the desired song | Integer | None |

## Output ##

| **Output Name** | **Description of Signal** | **Expected Range** |
|:----------------|:--------------------------|:-------------------|
| PWM | It is a signal that is fed to the speaker to play sound | 0-3.3V |

## Test Signal ##

| **T.P. Name** | **Description of Signal and measurement conditions** | **Range of Values** |
|:--------------|:-----------------------------------------------------|:--------------------|
| LEDs | To test visually which pins is selected to play sound from shift register to audio driver | 1-8 |


