# Capacitive Touch Research #



## Capacitive Touch Driver Options Summary ##

| **Brand** | **Part Number** | **Voltage** | **Current** | **Channels** | **Interface** | **Price** |
|:----------|:----------------|:------------|:------------|:-------------|:--------------|:----------|
|Azoteq|IQS333|1.8-3.6V|360μA|9 |I2C|$0.52|
|Atmel|AT42QT2120|1.8-5V|1095μA|12|I2C|$2.05|

## Driver Option 1 ##

I selected this driver because it meets all the requirements we need, as well as make some tasks easier for us. This chip has a built in slider function, which will help us be able to detect a swipe motion. It is also very cheap, and does not require a lot of power.

![http://i.imgur.com/sGxQl6p.gif](http://i.imgur.com/sGxQl6p.gif)

Image taken from [ISQ333 datasheet](http://www.mouser.com/catalog/specsheets/iqs333_datasheet.pdf).

## Driver Option 2 ##

This chip is listed as our alternative mainly because of cost. The chip costs almost four times as much as our first option. Much like the first chip, this one also supports sliders, which makes detecting swipe motions easier. Of the capacitive touch drivers I was able to find, there were not many that would support sliders, and of the ones that do this one seemed to stand out.

![http://i.imgur.com/EqVVrIh.gif](http://i.imgur.com/EqVVrIh.gif)

Image taken from [AT42QT2120 datasheet](http://www.mouser.com/catalog/specsheets/iqs333_datasheet.pdf).

## Capacitive Touch Surface Options ##

We will connect the capacitive touch driver to one of these types of materials for the user to interface with the crossbow.

### Option 1: Copper ###

Copper is one of the cheapest and common metals used for making PCBs. The easy and cheap access to this material as well as its ability to achieve the goal we desire is why it is our number one option.

### Option 2: Indium Tin Oxide ###

Indium Tin Oxide (ITO) is a fairly expensive option to use, but provides for some very cool applications. ITO comes in some forms that are transparent, which opens the door to creativity. As cool as it would be to use, the cost is too high to choose it over copper.

### Option 3: Nickel ###

There are a multitude of metals that are able to be used for this process. Nickel is among these metals, but because of the price difference between copper and these other metals they are placed as our last option.

## Capacitive Touch Logic Flow Chart ##

Flow chart for check\_touch() function

![http://i.imgur.com/SD74f53.gif](http://i.imgur.com/SD74f53.gif)

## Capacitive Touch Research Data Sources ##

| **Type of Datasource** | **Title, URL, etc.** | **Using in Prototype?** |
|:-----------------------|:---------------------|:------------------------|
|IQS333 Datasheet|http://www.mouser.com/catalog/specsheets/iqs333_datasheet.pdf|Yes|
|AT42QT2120 Datasheet|http://www.atmel.com/Images/doc9634.pdf|No|
|Online Article|http://www.analog.com/library/analogdialogue/archives/40-10/cap_sensors.html|No|
|Online Article|http://electronicdesign.com/components/self-capacitive-sensing-brings-touch-large-screens|No|