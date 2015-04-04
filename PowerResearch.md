# Power Research #


## Battery Options Research Summary ##

| **Name/Brand** | **Type** | **Voltage** | **Capacity** | **Recharging Method** | **Price** |
|:---------------|:---------|:------------|:-------------|:----------------------|:----------|
|Anker Astro Mini|Li Ion USB Battery Pack|5 volts|3000 mAh|USB|$19.99|
|Photive|Li Ion USB Battery Pack|5 volts|3000 mAh|USB|$19.95|
|Tenergy|Li Ion Batteries|7.4 volts|2600 mAH|External Recharger|$13.99 + cost of charger|

### Battery Option 1 ###
The battery I want to use is the Anker Astro Mini USB battery pack.  It has a capacity of 3000 mAh, but based on the manufacturer’s notes, it operates at 80% efficiency, giving a realistic capacity of 2400 mAh.  Our project’s max current draw is ~950 mA, so the two hour power requirement would be met under normal operating conditions.  It is internally regulated at 5 volts and can provide up to 1 amp.  With the addition of an external regulator circuit, I will be able to provide 3.3 volts and 5 volts to components in other blocks.  The battery pack is also very compact and lightweight, making it ideal for our arm-mounted crossbow.  It is rechargeable via its USB port, so creating charging circuitry is not necessary.

Available for purchase through Amazon [here](http://www.amazon.com/Anker-Astro-Mini-Ultra-Compact-Lipstick-Sized/dp/B005X1Y7I2).

### Battery Option 2 ###
Battery option 2 is the Photive 3000 mAh USB battery pack.  It is very similar to Option 1 in that it meets the power requirements, has its own 5 volts regulation, and is lightweight.  It also charges via its USB port.  The area that sets the Photive battery apart is its form factor.  It is a thin rectangle instead of a round tube (like the Anker Astro Mini).  This form factor could be simpler to integrate into our packaging.  It would be easier to create a 3D-printed container for a rectangular battery pack.

Available for purchase through Amazon [here](http://www.amazon.com/Photive-3000mAh-Portable-Battery-Charger/dp/B00BFY59BA).
 
### Battery Option 3 ###
The least favorable option is a Tenergy 7.4 volt/2600 mAh lithium ion battery.  Its capacity would most likely allow it to meet the 2 hour power requirement, but it requires external charging circuitry, which would easily cost another $20 (an example can be found here ).  It also has a less desirable form factor.  However, weighing about 3.5 ounces, it would still be acceptably lightweight for our arm-mounted crossbow.  Another disadvantage of using this battery is the fact that it is 7.4 volts.  This would require me to use separate regulators to supply other blocks with 5 volts and 3.3 volts.

Available for purchase through All-Battery.com [here](http://www.all-battery.com/li-ion1865074v2600mahbatterypcbmodulewith22awgbareleads.aspx).

## Voltage Regulator Options Research Summary ##

| **Brand** | **Type** | **Input Voltage** | **Output Voltage** | **Ouput Current** | **Price** |
|:----------|:---------|:------------------|:-------------------|:------------------|:----------|
|STMicroelectronics|Switching|2.8-5.5 V|0.8 V and up|3 A|$1.76|
|Micrel|Switching|2.7-5.5 V|0.95-3.6 V|2 A|$1.10|
|Micrel|LDO|0-6 V|3.3 V|1 A|$1.75|

### Voltage Regulator Option 1 ###
My first preference for voltage regulation is an IC chip made by STMicroelectronics.  It can accept input voltages anywhere between 2.8 and 5.5 volts and has an adjustable output voltage (with 3.3 volts being in the adjustable range) and can output up to 3 A. It is inexpensive, has a smaller footprint than other options, but requires several external components (inductor, capacitors, and diode) to set and maintain the desired output voltage.

Available from $1.76 at [Mouser](http://www.mouser.com/ProductDetail/STMicroelectronics/ST1S31D-R/?qs=%2fha2pyFadujk%252bkS6YOUnGQm8xeuFaql%2fzaQu9q2oKXnkti8h4e7JHw%3d%3d).

### Voltage Regulator Option 2 ###
This regulator is very similar to Option 1, but has the advantage of being less expensive and having an increased output current (2 A, but this is useless as the batteries can only supply 1 A). However, it has a larger footprint and requires more external components to set and maintain the output voltage.  The advantages do not outweigh the disadvantages.

Available from $1.10 at [Mouser](http://www.mouser.com/ProductDetail/Micrel/MIC23201YML-T5/?qs=sGAEpiMZZMtitjHzVIkrqSWA8dCfXyljfjts5jJf%252bEE%3d).

### Voltage Regulator Option 3 ###
In the interest of diversity, Option 3 is a LDO (linear drop out) regulator.  It has a fixed output voltage, so no external components are required to set and maintain the voltage.  However, it is more expensive and less efficient than switching regulators.

Available from $1.75 at [Mouser](http://www.mouser.com/ProductDetail/Micrel/MIC37100-33WS-TR/?qs=sGAEpiMZZMsGz1a6aV8DcP%252b6ey5cUOYk%252bCOaBvobf10%3d).

### USB Pin Out ###

Found at www.usbpinout.net.

## Power Research Data Sources ##

| **Type of Source** | **Title, URL, etc.** | **Using in Prototype?** |
|:-------------------|:---------------------|:------------------------|
|Web Article|[Selecting the Correct Regulator for Your Application](http://www.digikey.com/en-US/articles/techzone/2012/sep/selecting-the-correct-regulator-for-your-application)|Yes|
|Online Magazine|[Digital Power Management Done Right](http://cds.linear.com/docs/en/article/PET_EN_082009.pdf)|No|
|Archived Journal|[Considerations in Designing Single Supply...](http://www.analog.com/library/analogDialogue/archives/30-1/consider.html)|No|
|Online Blog|[Understanding Battery Capacity: Ah is not A](http://www.pololu.com/blog/2/understanding-battery-capacity-ah-is-not-a)|Yes|
|Web Article|[Power Supply Regulation](http://www.altera.com/support/devices/power/regulators/pow-regulators.html)|No|
|Instruction Manual|[Anker Astro Mini](http://www.ianker.com/download.php?file=download/10656E8B5C8C4D4_79AN3K-BA%20EN%20JP%20FR%20DE%20%20%202013-9-26.jpg)|Yes|
|Product Page|[Photive 3000 mAh Portable Battery Charger](http://www.amazon.com/Photive-3000mAh-Portable-Battery-Charger/dp/B00BFY59BA)|No|
|Data Sheet|[Tenergy 7.4 Volt Battery Pack](http://www.all-battery.com/datasheet/31004_datasheet.pdf)|No|
|Data Sheet|[STMicroelectronics Regulator](http://www.st.com/web/en/resource/technical/document/datasheet/DM00051589.pdf)|Yes|
|Data Sheet|[MIC23201](http://www.micrel.com/_PDF/MIC23201.pdf)|No|
|Data Sheet|[MIC37100](http://www.micrel.com/_PDF/mic37100.pdf)|No|
