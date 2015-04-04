# Capactive - Final Design #

The capacitive touch portion consists of a driver that will detect a change in capacitance of a conductive surface.  The conductive surfaces are arranged in a line.  Software is then used to determine if the touch gesture was a tap or swipe.   If a tap is detected and a bolt is not already loaded, a bolt will be loaded.  If a bolt is loaded and a swipe is detected, it will measure the distance swiped and will set a number of packets to fire corresponding to the swipe.  Finally, if a bolt is loaded, the packets have been set, and a tap is detected, the crossbow will fire.


![http://i.imgur.com/Bo6Dqj7.png](http://i.imgur.com/Bo6Dqj7.png)