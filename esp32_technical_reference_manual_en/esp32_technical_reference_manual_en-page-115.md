**Title:**
Chapter 6

**Subtitle:**
IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Title:**
6.1 Overview

**Body Text:**
The ESP32 chip features 34 physical GPIO pins. Each pin can be used as a general-purpose I/O, or be connected to an internal peripheral signal. The IO MUX^1, RTC IO MUX and the GPIO matrix are responsible for routing signals from the peripherals to GPIO pins. Together these systems provide highly configurable I/O.

Note that the I/O GPIO pins are 0-19, 21-23, 25-27, 32-39, while the output GPIOs are 0-19, 21-23, 25-27, 32-33. GPIO pins 34-39 are input-only.

GPIO20 serves as a valid input and output only on ESP32-PICO-V3 and ESP32-PICO-V3-02. Please refer to ESP32-PICO Series Datasheet for more information.

This chapter describes the signal selection and connection between the digital pins (FUN_SEL, IE, OE, WPU, WDU, etc.), 162 peripheral input and 176 output signals (control signals: SIG_IN_SEL, SIG_OUT_SEL, IE, OE, etc.), fast peripheral input/output signals (control signals: IE, OE, etc.), and RTC IO MUX.

**Figure Caption:**
Figure 6.1-1. IO MUX, RTC IO MUX and GPIO Matrix Overview

**Diagram Description in Text Format:**
The diagram shows the signal selection process for different types of pins such as SPI, UART, I²C, PWM, etc., which are connected to various functions like IO, OE, WPU, etc.

1. The IO MUX contains one register per GPIO pin. Each pin can be configured to perform a “GPIO” function.
   - ^MUX: Multiplexer. The ESP32 chip integrates multiple peripherals that require communication with the outside world. To keep the chip package size reasonably small, the number of available pins has to be limited. So the only way to route all the incoming and outgoing signals is through pin multiplexing. Pin muxing is controlled via software programmable registers such as IO_MUX_X_REG.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback