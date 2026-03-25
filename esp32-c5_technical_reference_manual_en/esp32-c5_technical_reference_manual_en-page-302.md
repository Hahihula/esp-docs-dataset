

# Chapter 8

## GPIO Matrix and IO MUX

### 8.1 Overview

GPIO matrix is a hardware structure that allows dynamic remapping between the GPIO pins and peripheral input/output signals to provide greater flexibility. IO MUX (Input/Output Multiplexing) is a technology that allows the same pin to perform different functions at different times, allowing dynamic switching of pin functions through configuration.

ESP32-C5 provides two groups of GPIO matrix and IO MUX:

* HP GPIO matrix and HP IO MUX
* LP GPIO matrix and LP IO MUX

The ESP32-C5 chip features 29 GPIO pins, numbered from GPIO0 to GPIO28, including

* 7 LP GPIO pins (GPIO0~GPIO6) for either HP or LP peripherals.
* 14 HP GPIO pins (GPIO7~GPIO14, GPIO23~GPIO28) for HP peripherals only.
* 8 dedicated GPIO pins (GPIO15~GPIO22) for external flash and PSRAM. These pins can not be used for other purpose, and therefore are not described in subsequent sections. For more information regarding these pins, please refer to ESP32-C5 Datasheet > Section Pin Mapping Between Chip and Flash/PSRAM.

Each pin can be used as a general-purpose I/O, or be connected to an internal peripheral signal. Together these modules provide highly configurable I/O.

* Through HP GPIO matrix and HP IO MUX, HP peripheral input signals can be from any GPIO pins, and HP peripheral output signals can be routed to any GPIO pins.
* Through LP GPIO matrix and LP IO MUX, LP peripheral input signals can be from any LP GPIO pins, and LP peripheral output signals can be routed to any LP GPIO pins.

Unless otherwise specified, GPIO matrix refers to both LP GPIO matrix and HP GPIO matrix, so as to IO MUX.

### 8.2 Features

#### 8.2.1 HP GPIO Matrix and HP IO MUX

HP GPIO matrix has the following features:

* A full-switching matrix between HP peripheral input/output signals and the GPIO pins
* 76 HP peripheral input signals sourced from the input of any GPIO pins