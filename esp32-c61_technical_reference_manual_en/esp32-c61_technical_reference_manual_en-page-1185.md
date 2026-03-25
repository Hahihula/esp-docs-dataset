

# Chapter 32

## Temperature Sensor

### 32.1 Overview

ESP32-C61 provides a temperature sensor to monitor temperature changes inside the chip in real time. The sensor converts analog voltage to digital values and supports compensation for the temperature offset.

### 32.2 Features

The temperature sensor has the following features:

*   Software-triggered temperature measurement. Once triggered, the sensor continuously measures temperature. Software can read the data any time.
*   Hardware-triggered automatic temperature monitoring
*   Two modes for automatic monitoring of temperature and support for triggering interrupts
*   Configurable temperature offset based on the application scenario for improved accuracy
*   Configurable temperature measurement range
*   Support for several Event Task Matrix (ETM) related events and tasks

### 32.3 Architecture

Figure 32.3-1 shows the internal structure of the temperature sensor.