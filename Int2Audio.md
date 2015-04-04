# Audio - Final Design #

The Audio driver outputs sound whenever one of the following situations occurs: firing bolts, reloading bolts, hit by enemy, or cool-down period. Therefore, when one of the situations occurs, the MCU plays the correct sound. The method of saving the sound into the driver is by recording it through a built-in microphone. In order to playback or record sounds, a switch needs to be used so that a low voltage for recording and a high voltage for playback. Also, if the desired sound needs to be played, then its pin needs to be set low.

![http://i.imgur.com/YbrLm2a.png](http://i.imgur.com/YbrLm2a.png)