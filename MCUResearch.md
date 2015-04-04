# Microcontroller Research #


## Microcontroller Options Summary ##

| **Brand** | **Model** | **I/O Pins** | **CAN Module** | **Price** |
|:----------|:----------|:-------------|:---------------|:----------|
|Microchip|PIC24HJ64GP502|21|Yes|$4.78(free samples)|
|Microchip|PIC24HJ64GP504|35|Yes|$4.93 (free samples)|
|Texas Instruments|MSP430F2410|55|No|$4.60 (free samples)|

### Microcontroller Option 1 ###
The first choice for the microcontroller is the PIC24HJ64GP502. It is a 28-pin package that has modules for all of the communication protocols we need (I2C, SPI, and CAN). The 28-pin package was chosen because it has enough I/O pins for every block that interfaces with the microcontroller. Additionally, a PIC chip was chosen due to the large amount of reference material available, and the design lab’s software and hardware support for developing with PIC chips.

### Microcontroller Option 2 ###
The second choice is the PIC24HJ64GP504, which is the bigger brother of the first chip. It has more I/O pins, but still uses the same core and same code structure. It would be used in the situation where a different block has to change and then requires more I/O pins to function. This chip would facilitate the code adaptation from the first option.

### Microcontroller Option 3 ###
An MSP430 chip is the third option. It would be a fallback if we could get absolutely nothing working on the PIC chips. Additionally, it does not support CANbus natively, so we would need an external chip.

## Programming Options ##
**Option 1:** A main loop that polls the I2C module for input, and has an interrupt for IR input.

**Option 2:** A main loop that has interrupts for IR and I2C input.

**Option 3:** A main loop that polls both I2C and the IR input pin.

### Programming Option 1 ###
Option 1 was chosen because of the simplicity of handling a single interrupt. For polling I2C, a touch function will be called that handles the I2C input. For the IR interrupt, an IR function will be called that handles the input. Since the IR input will not be buffered, it is critical that the input is handled as soon as possible, therefore an interrupt is used. The I2C on the PIC chip is double buffered for receiving, so it is not as time-critical.

### Programming Option 2 ###
Option 2 will be used in the case that I2C requires immediate handling. In this case, an additional program-created buffer will be filled when the I2C interrupt happens, and then control will immediately be handed back to the previous execution (allowing for time-critical code such as IR input). The I2C data will then be processed by the standard touch function in the main loop. Additionally, the touch functions will have to be redefined if option 2 is enacted.

### Programming Option 3 ###
This option will only be used in the case that we absolutely cannot get interrupts working on the microcontroller. It would aggressively poll the IR input and store values into RAM, and have the IR function handle it when the buffer reaches a specified length. The same procedure would be used for I2C input. Again, the touch and IR functions will have to be redefined if option 3 is enacted.

## Public Functions for Each Block ##
The functions provided by the individual blocks that MCU integration will use are as follows:

### Visual Logic ###
```

void update_battery(integer) – displays battery status

void update_ammo(integer) – displays ammo count

void update_health(integer) – displays amount of health

void update_load(Boolean) – displays if bolt is loaded

void fire_display(Boolean) – displays that a bolt is firing

void cooldown_display(integer) – displays current cooldown in seconds

void update_led_bar(integer) – updates current amount of LEDs lit on bar

```

### Touch Logic ###
```

touch will be a C struct that holds data about a touch event (tap or swipe, swipe strength).

touch check_touch(void) – handles I2C input and gives back touch data

void touch_init(void) – handles initializing I2C and the touch controller

```

### CAN Logic ###
```

bool im_dead(void) – sends an “I’m dead” packet over CAN, and returns true if successful

```

### Sound Logic ###
```

void play_sound(integer) – play a specified sound

```

### IR Logic ###
```
integer receive_packet(void) – handles IR input and returns a damage/healing value

void shoot_packet(integer) – shoots a MIRP packet at the specified strength level

```