

# Chapter 25

## UART Controller (UART)

### 25.1 Overview

A UART is a character-oriented data link for asynchronous communication between devices. Such communication does not add clock signals to the data sent. Therefore, in order to communicate successfully, the transmitter and the receiver must operate at the same baud rate with the same stop bit(s) and parity bit(s).

A UART data frame usually begins with one start bit, followed by data bits, one parity bit (optional), and one or more stop bits. UART controllers on ESP32-C61 support various lengths of data bits and stop bits. This allows developers to use multiple UART ports at minimal software cost.

ESP32-C61 has two UART controllers. These UARTs are compatible with various UART devices, and support Infrared Data Association (IrDA) and RS485 communication. In this chapter, the two regular UART controllers are referred to as `UARTn`, in which *n* denotes 0, 1.

### 25.2 Features

UART controllers feature:

- Programmable baud rate up to 5 MBaud
- 128 x 8 bit RAM respectively for the TX channel and RX channel of a UART controller
- Full-duplex asynchronous communication
- Data bits (5 to 8 bits)
- Stop bits (1, 1.5, or 2 bits)
- Parity bit
- Special character AT_CMD detection
- RS485 protocol
- IrDA protocol
- Receive timeout
- UART as wakeup source
- Software and hardware flow control
- Three prescalable clock sources:
    1. XTAL_CLK
    2. RC_FAST_CLK