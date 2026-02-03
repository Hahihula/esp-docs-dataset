**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Titles with Subsections**

1. **6.1 Overview**
   - The ESP32-S3 chip features 45 physical GPIO pins.
   - Each pin can be used as a general-purpose I/O or connected to an internal peripheral signal through GPIO matrix and IO MUX.

2. **6.2 Features**

   #### GPIO Matrix Features
   - A full-switching matrix between the peripheral input/output signals and the GPIO pins.
   - 175 digital peripheral input signals can be sourced from any of the 45 GPIO pins output or input.
   - The output signal is routed to one of the 184 digital peripheral outputs.

   #### IO MUX Features
   - Provides configuration register IOMUX_GPIO_n_REG for each GPIO pin, allowing GPIO function routing and bypassing the matrix directly connected to GPIO functions (SPI, JTAG, UART).
   - Supports high-speed signals like SPI, JTAG, UART.
   - Redirects 22 RTC input/output signals.

3. **RTC IO MUX Features**
   - Controls low power features of 22 RTC GPIO pins and analog functions for better performance in digital peripherals (SPI).

**Footer:**
- Page number: 472
- Document version: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems

**Navigation Link:** GoBack