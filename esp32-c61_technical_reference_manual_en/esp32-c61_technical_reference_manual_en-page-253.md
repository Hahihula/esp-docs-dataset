

# Chapter 6

## GPIO Matrix and IO MUX

### 6.1 Overview

GPIO matrix is a hardware structure that allows dynamic remapping between the GPIO pins and peripheral input/output signals to provide greater flexibility. IO MUX (Input/Output Multiplexing) is a technology that allows the same pin to perform different functions at different times, allowing dynamic switching of pin functions through configuration.

ESP32-C61 provides two groups of GPIO matrix and IO MUX:

- HP GPIO matrix and HP IO MUX
- LP GPIO matrix and LP IO MUX

The ESP32-C61 chip features 30 GPIO pins, numbered from GPIO0 to GPIO29, including

- 7 LP GPIO pins (GPIO0~GPIO6) for either HP or LP peripherals.
- 15 HP GPIO pins (GPIO7~GPIO13, GPIO22~GPIO29) for HP peripherals only.
- 8 dedicated GPIO pins (GPIO14~GPIO21) for external flash or PSRAM. These pins can not be used for other purpose, and therefore are not described in subsequent sections. For more information regarding these pins, please refer to ESP32-C61 Datasheet > Section Pin Mapping Between Chip and Flash/PSRAM.

Each pin can be used as a general-purpose I/O, or be connected to an internal peripheral signal. Together these modules provide highly configurable I/O.

- Through HP GPIO matrix and HP IO MUX, HP peripheral input signals can be from any GPIO pins, and HP peripheral output signals can be routed to any GPIO pins.
- Through LP GPIO matrix and the LP IO MUX, the LP system can be configured to simple GPIO input/output and GPIO wake-up functions.

Unless otherwise specified, GPIO matrix refers to both LP GPIO matrix and HP GPIO matrix, so as to IO MUX.

### 6.2 Features

#### 6.2.1 HP GPIO Matrix and HP IO MUX

HP GPIO matrix has the following features:

- A full-switching matrix between HP peripheral input/output signals and the GPIO pins
- 36 HP peripheral input signals sourced from the input of any GPIO pins