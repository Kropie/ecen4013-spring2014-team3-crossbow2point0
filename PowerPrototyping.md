# Power Block Prototyping #



## Detailed Block Diagram ##

![http://i.imgur.com/Uw9aJgD.gif](http://i.imgur.com/Uw9aJgD.gif)

## Schematic ##

![http://i.imgur.com/vUJBCxU.png](http://i.imgur.com/vUJBCxU.png)

## Hardware Inputs ##

| **Input Name** | **Description of Signal** |
|:---------------|:--------------------------|
| USB Charging | The USB battery pack is charged via the USB standard 5 volts at 1 amp.  You can also give it more than 1 amp by using a wall-wart-type MicroUSB charger (such as is used for an Android phone).|


## Hardware Outputs ##

| **Output Name** | **Description of Signal** | **Expected Range** |
|:----------------|:--------------------------|:-------------------|
| 5 Volt Output | This output provides 5 volts for our CANbus transceiver, which is the only component that requires 5 volts.  It requires less than 50 mA.| 4.8-5.1 volts, 50 mA |
| 3.3 Volt Output | This output provides 3.3 volts for the rest of the blocks in our project.  The rest of the project requires around 500 mA. | 3.2-3.4 volts, 500 mA|

## Signals at Test Points ##

| **T.P.Name** | **Description of Signal and measurement conditions** | **Range of Values** |
|:-------------|:-----------------------------------------------------|:--------------------|
| TP1 | This is the voltage directly across the USB battery terminals.  As load increases, this voltage can sag significantly. | 3-5.1 volts |
| TP2 | This is the voltage on the output of the 5 volt boost regulator. | 4.8-5.1 volts |
| TP3 | This is the voltage on the output of the 3.3 volt buck regulator. | 3.2-3.4 volts |

## Current-Voltage Output Data ##

| **Time** | **Voltage Across the Output** | **Current Through Load** | **Load Value** |
|:---------|:------------------------------|:-------------------------|:---------------|
|0 |3.44|530|6.154|
|10|3.39|530|6.154|
|20|3.399|531|6.154|
|30|3.401|532|6.154|
|40|3.401|535|6.154|
|50|3.423|536|6.154|
|60|3.421|535|6.154|
|70|3.422|536|6.154|
|80|3.422|536|6.154|
|90|3.407|532|6.154|
|100|3.412|532|6.154|
|110|3.413|533|6.154|
|120|3.421|532|6.154|
|130|3.424|536|6.154|

## 3.3 Volt Output Current-Voltage Plot ##

![http://i.imgur.com/wUOlZ5f.gif](http://i.imgur.com/wUOlZ5f.gif)

## Prototyping Images ##

### 5 Volt Boost Regulator ###

![http://i.imgur.com/RvgR9lt.jpg](http://i.imgur.com/RvgR9lt.jpg)

### 3.3 Volt Buck Regulator ###

![http://i.imgur.com/Aeyaprg.jpg](http://i.imgur.com/Aeyaprg.jpg)

### USB Battery with Both Regulators ###

![http://i.imgur.com/FtCvYR6.jpg](http://i.imgur.com/FtCvYR6.jpg)