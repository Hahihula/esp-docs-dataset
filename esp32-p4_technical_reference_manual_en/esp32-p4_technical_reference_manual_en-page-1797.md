

# Chapter 38

## LCD and Camera Controller (LCD_CAM)

### 38.1 Overview

The LCD and Camera controller (LCD_CAM) on the ESP32-P4, consisting of an independent LCD control module and a camera control module, is a versatile component designed to facilitate interfacing with both LCDs and cameras.

The LCD module provides an LCD interface that can connect to RGB, Motorola 6800 (MOTO6800), and Intel 8080 (I8080) compatible LCD devices. The LCD module is responsible for sending video data to the display.

The Camera module provides one parallel camera interface that can connect to external digital video port (DVP) cameras in 8/16-bit modes. It manages communication with the camera to capture images or video frames.

The LCD_CAM controller offers flexibility for projects that involve both displaying information on screens and working with cameras for image or video processing.

### 38.2 Features

LCD_CAM has the following features:

- Supports the following operation modes:
    - LCD master TX mode
    - Camera slave RX mode
    - Camera master RX mode

- Supports simultaneous connection to an external LCD and a camera

- When interfacing with an external LCD, the following is supported:
    - 8/16/24-bit parallel output modes
    - RGB, MOTO6800, and I8080 LCD formats
    - LCD data retrieved from internal memory or external memory via GDMA

- When interfacing with an external camera (i.e., DVP image sensor), the following is supported:
    - 8/16-bit parallel input modes
    - Camera data stored in internal or external memory via GDMA

- Supports interrupts