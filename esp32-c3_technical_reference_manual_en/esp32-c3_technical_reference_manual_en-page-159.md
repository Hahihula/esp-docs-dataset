

```markdown
Chapter 5

IO MUX and GPIO Matrix (GPIO, IO MUX)

5.1 Overview

The ESP32-C3 chip features 22 physical GPIO pins. Each pin can be used as a general-purpose I/O, or be connected to an internal peripheral signal. Through GPIO matrix and IO MUX, peripheral input signals can be from any IO pins, and peripheral output signals can be routed to any IO pins. Together these modules provide highly configurable I/O.

Note that the GPIO pins are numbered from 0 ~ 21.

5.2 Features

GPIO Matrix Features
* A full-switching matrix between the peripheral input/output signals and the pins.
* 42 peripheral input signals can be sourced from the input of any GPIO pins.
* The output of any GPIO pins can be from any of the 78 peripheral output signals.
* Supports signal synchronization for peripheral inputs based on APB clock bus.
* Provides input signal filter.
* Supports sigma delta modulated output.
* Supports GPIO simple input and output.

IO MUX Features
* Provides one configuration register IO_MUX_GPIOn_REG for each GPIO pin. The pin can be configured to
  - perform GPIO function routed by GPIO matrix;
  - or perform direct connection bypassing GPIO matrix.
* Supports some high-speed digital signals (SPI, JTAG, UART) bypassing GPIO matrix for better high-frequency digital performance. In this case, IO MUX is used to connect these pins directly to peripherals.

5.3 Architectural Overview

This section provides an overview to the architecture of IO MUX and GPIO matrix with the following figures:

* Figure 5.3-1 shows the general work flow of IO MUX and GPIO matrix.
```