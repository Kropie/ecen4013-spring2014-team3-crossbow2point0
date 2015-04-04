# Power - Final Design #

The power supply consists of two voltage regulators connected to a five volt, 3000 mAh USB battery back, which is theoretically capable of outputting one amp.  The first regulator is a five volt boost regulator.  This regulator is necessary because, under load, the USB battery drops anywhere from 0.5 volts to 2 volts across its internal resistance, giving only a three volt output.  Cascaded from the output of the five volt boost regulator is a 3.3 volt buck regulator.  This regulator is necessary to provide 3.3 volts to other blocks (such as the MCU, Visual Display, and Audio).  Both regulators maintain their set voltages even under load, rated up to 1.5 amps.

![http://i.imgur.com/8faM5uf.png](http://i.imgur.com/8faM5uf.png)