

# Chapter 7
## Chip Boot Control

### 7.1 Overview

ESP32-C3 has three strapping pins:

* GPIO2
* GPIO8
* GPIO9

These strapping pins are used to control the following functions during chip power-on or hardware reset:

* control chip boot mode
* ROM code printing

During power-on reset, RTC watchdog reset, brownout reset, analog super watchdog reset, and crystal clock glitch detection reset (see Chapter 6 Reset and Clock), hardware captures samples and stores the voltage level of strapping pins as strapping bit of "0" or "1" in latches, and holds these bits until the chip is powered down or shut down. Software can read the latch status (strapping value) from GPIO_STRAPPING.

By default, GPIO9 is connected to the chip's internal pull-up resistor. If GPIO9 is not connected or connected to an external high-impedance circuit, the internal weak pull-up determines the default input level of this strapping pin (see Table 7.1-1).

Table 7.1-1. Default Configuration of Strapping Pins

| Strapping Pin | Default Configuration |
|---------------|------------------------|
| GPIO2         | N/A                    |
| GPIO8         | N/A                    |
| GPIO9         | Pull-up                |

To change the strapping bit values, users can apply external pull-down/pull-up resistors, or use host MCU GPIOs to control the voltage level of these pins when powering on ESP32-C3. After the reset is released, the strapping pins work as normal-function pins.

**Note:**
The following section provides description of the chip functions and the pattern of the strapping pins values to invoke each function. Only documented patterns should be used. If some pattern is not documented, it may trigger unexpected behavior.