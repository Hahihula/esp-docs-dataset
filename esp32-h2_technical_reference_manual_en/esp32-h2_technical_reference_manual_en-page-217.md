

```markdown
Chapter 6

IO MUX and GPIO Matrix (GPIO, IO MUX)

6.1 Overview

The ESP32-H2 chip features 19 GPIO pins. Each pin can be used as a general-purpose I/O, or be connected to an internal peripheral signal. Through GPIO matrix and IO MUX, peripheral input signals can be from any IO pins, and peripheral output signals can be routed to any IO pins. Together these modules provide highly configurable I/O.

Note that the GPIO pins are numbered from GPIO0 ~ GPIO5, GPIO8 ~ GPIO14, and GPIO22 ~ GPIO27.

6.2 Features

GPIO matrix has the following features:

- A full-switching matrix between the peripheral input/output signals and the GPIO pins.
- 78 peripheral input signals sourced from the input of any GPIO pins.
- 99 peripheral output signals routed to the output of any GPIO pins.
- Signal synchronization for peripheral inputs based on IO MUX operating clock. For more information about the operating clock of IO MUX, please refer to Section 7 Reset and Clock.
- GPIO Filter hardware for input signal filtering.
- Glitch Filter hardware for second time filtering on the input signal.
- Sigma delta modulated (SDM) output.
- GPIO simple input and output.

IO MUX has the following features:

- Better high-frequency digital performance achieved by some digital signals (SPI, JTAG, UART) bypassing GPIO matrix. In this case, IO MUX is used to connect these pins directly to peripherals.
- A configuration register IO_MUX_GPIOn_REG provided for each GPIO pin. The pin can be configured to
  - perform GPIO function routed by GPIO matrix;
  - or perform direct connection bypassing GPIO matrix.

6.3 Architectural Overview

Figure 6.3-1 shows in details how GPIO matrix and IO MUX route signals from pins to peripherals, and from peripherals to pins.
```