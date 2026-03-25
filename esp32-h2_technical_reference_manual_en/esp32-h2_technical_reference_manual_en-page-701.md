

# Chapter 28

## UART Controller (UART)

### 28.1 Overview

In embedded system applications, data is required to be transferred in a simple way with minimal system resources. This can be achieved by a Universal Asynchronous Receiver/Transmitter (UART), which flexibly exchanges data with other peripheral devices in full-duplex mode. ESP32-H2 has two UART controllers. These UARTs are compatible with various UART devices, and support Infrared Data Association (IrDA) and RS485 communication.

Each of the two UART controllers has a group of registers that function identically. In this chapter, the two UART controllers are referred to as `UARTn`, in which *n* denotes 0 or 1.

A UART is a character-oriented data link for asynchronous communication between devices. Such communication does not add clock signals to the data sent. Therefore, in order to communicate successfully, the transmitter and the receiver must operate at the same baud rate with the same stop bit(s) and parity bit.

A UART data frame usually begins with one start bit, followed by data bits, one parity bit (optional), and one or more stop bits. UART controllers on ESP32-H2 support various lengths of data bits and stop bits. These controllers also support software and hardware flow control as well as GDMA for high-speed data transfer. This allows developers to use multiple UART ports at minimal software cost.

### 28.2 Features

UART controllers feature:

*   Programmable baud rate up to 5 MBaud
*   128 x 8 bit RAM respectively for the TX channel and RX channel of a UART controller
*   Full-duplex asynchronous communication
*   Data bits (5 to 8 bits)
*   Stop bits (1, 1.5, or 2 bits)
*   Parity bit
*   Special character AT_CMD detection
*   RS485 protocol
*   IrDA protocol
*   High-speed data communication using GDMA