**Chapter Title:**
Chapter 22

**Subheading and Section Number:**
I2S Controller (I2S)
22.1 Overview

**Body Text:**

The I2S bus provides a flexible communication interface for streaming digital data in multimedia applications, especially digital audio applications. The ESP32 includes two I2S interfaces: I2S0 and I2S1.

The I2S standard bus defines three signals: a clock signal, a channel selection signal, and a serial data signal.
A basic I2S data bus has one master and one slave. The roles remain unchanged throughout the communication. The I2S modules on the ESP32 provide separate transmit and receive channels for high performance.

**Figure Description with Caption (Figure 22.1-1):**
I2S System Block Diagram

**Caption:**

Figure 22.1 is the system block diagram of the ESP32 I2S module. In the figure above, the value of "n" can be either 0 or 1. There are two independent I2S modules embedded in ESP32, namely I2S0 and I2S1. Each I2S module contains a Tx (transmit) unit and a Rx (receive) unit. Both the Tx unit and the Rx unit have a three-wire interface that includes a clock line, a channel selection line and a serial data line. The serial data line of the Tx unit is fixed as output, and the serial data line of the Rx unit is fixed as input. The clock line and the channel selection line of the Tx and Rx units can be configured to both master transmitting mode and slave receiving mode. In the LCD module, the serial data line extends to the parallel data bus. Both the Tx unit and the Rx unit have a 32-bit-wide FIFO with a depth of 64. Besides, only I2S0 supports on-chip DAC/ADC modes.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)