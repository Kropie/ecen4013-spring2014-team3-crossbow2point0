## Requirements for the Crossbow ##

Requirements were taken directly from the <a href='http://ecen4013.okstate.edu/docs/project2/sp2014/Spring2014-Crossbow2.pdf'>requirements sheet</a> on the ECEN 4013 website.

In the MAGE gaming environment, it can be beneficial to have a weapon with high accuracy and adjustable range. The crossbow emits narrow IR beam MIRP packets to incinerate enemies. The crossbow must also have an adjustable IR range. A loaded bolt can be drawn by the user and released at any time. It can be destroyed or damaged via IR attacks.

1. General Description

  * The crossbow is an arm mounted weapon capable of emitting and receiving MIRP packets.

  * The crossbow will use a system of swipe and tap gestures to control the crossbow.

2. Communication with the MAGE system

  * The crossbow must communicate with the user's HIU system over CANbus.

  * It must be able to take damage from only valid enemy MIRP packets.

  * It must transmit an “Im Dead” packet through CANbus to the HIU when the crossbow has been destroyed.

3. Crossbow mechanics

  * The crossbow will take in inputs from the user, utilizing swipe and tap gesture commands i.e. using capacitive touch or touchscreen/GUI.

  * The crossbow firing mechanism will be controlled using swipe gestures.

  * The loading and reloading mechanism will be controlled using tap gestures.

  * There should be a cool down period between firing consecutive shots.

4. MIRP transmission and reception

  * The crossbow must be able to transmit valid MIRP attack packets, at varying distances.

  * The distance is proportional to the strength of the swipe gesture.

  * Distances should be from 5-45 feet at 5 feet increments with no more than 10% error rate at the max distance, and no more than a 15 degree spread.

  * The crossbow must be able to receive valid MIRP packets from all angles.

5.Visual and audio indication

  * The crossbow must indicate visually and audibly when a bolt has been loaded.

  * It must indicate visually and audibly when a bolt has been fired and when the crossbow has been hit by an enemy MIRP attack.

  * The crossbow must indicate to the user how many bolts remain.

6. Form factor and casing
  * The crossbow should arm mounted with minimal wire exposure.

  * All circuit boards and power supplies should be enclosed/packaged appropriately.

  * Casing must be visually appealing.

7. Power
  * The crossbow must be powered with an internal power supply.

  * The crossbow should be able to operate through at least 2 hours of game play.