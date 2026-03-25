

# Chapter 39

## Temperature Sensor (TSENS)

### 39.1 Overview

ESP32-H2 provides a temperature sensor to monitor temperature changes inside the chip in real time. The sensor converts analog voltage to digital values and supports compensation for the temperature offset.

### 39.2 Features

The temperature sensor has the following features:

*   Software-triggered temperature measurement. Once triggered, the sensor continuously measures temperature. Software can read the data any time.
*   Hardware-triggered automatic temperature monitoring
*   Two wake-up modes for automatic temperature monitoring
*   Configurable temperature offset based on the application scenario for improved accuracy
*   Configurable temperature measurement range
*   Support for several Event Task Matrix (ETM) related events and tasks

### 39.3 Architecture

Figure 39.3-1 shows the internal structure of the temperature sensor.