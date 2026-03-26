

# 38.3 Functional Description

## 38.3.1 Block Diagram

Figure 38.3-1 shows the structure of LCD_CAM which includes:

* One TX control unit (LCD_Ctrl)
* One RX control unit (Camera_Ctrl)
* One asynchronous TX FIFO (Async TX FIFO) for communicating with external devices, e.g., LCDs
* One asynchronous RX FIFO (Async RX FIFO) for communicating with external devices, e.g., cameras
* Two clock generators (LCD_Clock Generator and CAM_Clock Generator) for generating clocks for each module
* Two format converters (RGB/YUV Converter) for converting video data into various formats

Figure 38.3-1. LCD_CAM Block Diagram

## 38.3.2 Signal Description

Table 38.3-1 shows the input and output signals required for the operation of the LCD and Camera controller.

The definition of the three operation modes is as follows:

* Camera Slave RX Mode: In this mode, the Camera module is the receiver of control signals.
* Camera Master RX Mode: In this mode, the Camera module sends clock signals to the slave, which will transmit data to the master upon receiving the signals.
* LCD Master TX Mode: In this mode, the LCD module initiates communication with the slave and sends control signals to the slave.