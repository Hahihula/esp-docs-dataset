

# Chapter 7

## IO MUX and GPIO Matrix (GPIO, IO MUX)

### 7.1 Overview

The ESP32-C6 chip features 31 GPIO pins. Each pin can be used as a general-purpose I/O, or be connected to an internal peripheral signal. Through GPIO matrix, IO MUX, and low-power (LP) IO MUX, peripheral input signals can be from any IO pins, and peripheral output signals can be routed to any IO pins. Together these modules provide highly configurable I/O.

**Note:**
- The 31 GPIO pins are numbered from GPIO0 ~ GPIO30.
- For chip variants without an in-package flash, GPIO14 is not led out to any chip pins, so GPIO14 is not available to users.
- For chip variants with an in-package flash, GPIO24 ~ GPIO30 are dedicated to connecting the in-package flash, not for other uses. GPIO10 ~ GPIO11 are not led out to any chip pins, thus not available to users. The remaining 22 GPIO pins (numbered GPIO0 ~ GPIO9, GPIO12 ~ GPIO23) are configurable by users.

### 7.2 Features

GPIO matrix has the following features:

- A full-switching matrix between the peripheral input/output signals and the GPIO pins.
- 85 peripheral input signals sourced from the input of any GPIO pins.
- 93 peripheral output signals routed to the output of any GPIO pins.
- Signal synchronization for peripheral inputs based on IO MUX operating clock. For more information about the operating clock of IO MUX, please refer to Section 8 Reset and Clock.
- GPIO Filter hardware for input signal filtering.
- Glitch Filter hardware for second time filtering on input signal.
- Sigma delta modulated (SDM) output.
- GPIO simple input and output.

IO MUX has the following features:

- Better high-frequency digital performance achieved by some digital signals (SPI, JTAG, UART) bypassing GPIO matrix. In this case, IO MUX is used to connect these pins directly to peripherals.
- A configuration register `IO_MUX_GPIOn_REG` provided for each GPIO pin. The pin can be configured to