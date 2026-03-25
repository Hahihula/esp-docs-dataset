

# Chapter 32

## UART Controller (UART)

### 32.1 Overview

A UART is a character-oriented data link for asynchronous communication between devices. Such communication does not add clock signals to the data sent. Therefore, in order to communicate successfully, the transmitter and the receiver must operate at the same baud rate with the same stop bit(s) and parity bit(s).

A UART data frame usually begins with one start bit, followed by data bits, one parity bit (optional), and one or more stop bits. UART controllers on ESP32-C5 support various lengths of data bits and stop bits. These controllers also support software and hardware flow control as well as GDMA for high-speed data transfer. This allows developers to use multiple UART ports at minimal software cost.

ESP32-C5 has three UART controllers, including two regular UARTs and one low-power (LP) UART. These UARTs are compatible with various UART devices, and support Infrared Data Association (IrDA) and RS485 communication. In this chapter, the two regular UART controllers are referred to as UARTn, in which n denotes 0, 1. LP UART is the cut-down version of the regular UART, with a separate group of registers. For differences between UART and LP UART, please refer to Table 32.2-1.

### 32.2 Features

Table 32.2-1 lists the feature comparison between UART and LP UART:

**Table 32.2-1. UART and LP UART Feature Comparison**

| UART Feature | LP UART Feature |
|--------------|------------------|
| Programmable baud rate up to 5 MBaud | |
| 128 x 8 bit RAM respectively for the TX channel and RX channel of a UART controller | 20 x 8-bit RAM, shared by the TX FIFO and RX FIFO of LP UART |
| Full-duplex asynchronous communication | |
| Data bits (5 to 8 bits) | |
| Stop bits (1, 1.5, or 2 bits) | |
| Parity bit | |
| Special character AT_CMD detection | |
| RS485 protocol | – |
| IrDA protocol | – |

Cont'd on next page