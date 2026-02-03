**Title:**
Chapter 8

**Subtitle:**
Chip Boot Control

**Section Title:**
8.1 Overview

**Body Text:**

ESP32-S3 has four strapping pins:
- GPIO0
- GPIO3
- GPIO45
- GPIO46

These strapping pins are used to control the following functions during chip power-on or hardware reset:

- control chip boot mode
- enable or disable ROM messages printing
- control the voltage of VDD_SPI
- control the source of JTAG signals

During Chip Reset (see Chapter 7 Reset and Clock), hardware captures samples and stores the voltage level of strapping pins as strapping bit of “0” or “1” in latches, and holds these bits until the chip is powered down or shut down. Software can read the latch status (strapping value) from the register GPIO_STRAPPING.

By default, GPIO0, GPIO45, and GPIO46 are connected to the chip’s internal pull-up/pull-down resistors. If these pins are not connected or connected to an external high-impedance circuit, the internal weak pull-up/pull-down determines the default input level of these strapping pins (see Table 8.1-1).

**Table Title:**
Table 8.1-1. Default Configuration of Strapping Pins

| Strapping Pin | Default Configuration |
|---------------|-----------------------|
| GPIO0         | Pull-up               |
| GPIO3         | N/A                   |
| GPIO45        | Pull-down             |
| GPIO46        | Pull-down             |

**Additional Information:**
To change the strapping bit values, users can apply external pull-down/pull-up resistors, or use host MCU GPIOs to control the voltage level of these pins when powering on ESP32-S3. After the reset is released, the strapping pins work as normal-function pins.

**Footer:**
Espressif Systems  
534  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback]