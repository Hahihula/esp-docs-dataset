**4 Functional Description**

The pins for the LP-SPI interface can be chosen from any pins via the LP GPIO Matrix.

---

**4.2.2.3 I2C Controller (I2C)**

ESP32-P4 has three I2C controllers: two in the main system and one in the low-power system. The two I2C controllers in the main system can act as a master or a slave (referred to as I2C below), while the one in the low-power system can only act as a master (referred to as LP_I2C below), which can still work when the main system sleeps.

**Feature List**

The I2C controller of ESP32-P4 has the following features:

- Master mode and slave mode
- Communication between multiple masters and slaves
- Standard mode (100 Kbit/s)
- Fast mode (400 Kbit/s)
- 7-bit addressing and 10-bit addressing
- Continuous data transfer achieved by pulling SCL low in slave mode
- Programmable digital noise filtering
- Dual address mode, which uses slave address and slave memory or register address

**Pin Assignment**

For I2C, the pins used can be chosen from any GPIOs via the GPIO Matrix.
For LP I2C, the pins used can be chosen from any GPIOs via the LP GPIO Matrix.

---

**4.2.2.4 Analog I2C Controller**

This module is a dedicated I2C host that communicates with some analog modules to configure parameters of these modules. Each configurable module has an I2C slave with its own address.

**Feature List**

- Master mode only
- 7-bit addressing
- Adjustable transmission rate
- Communication in the sleep modes supported by the Low-Power CPU
- Dual master operation mode

**Pin Assignment**

The analog I2C interface connects internal analog components without requiring allocating IO pins. 

---

Espressif Systems  
64  
ESP32-P4 Series Datasheet v0.6  

[Submit Documentation Feedback](#)