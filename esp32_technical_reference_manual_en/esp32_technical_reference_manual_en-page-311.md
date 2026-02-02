**Chapter Title:**
Chapter 19 UART Controller (UART)

**GoBack Link:** [GoBack](#)

---

### 19.1 Overview

Embedded applications often require a simple method of exchanging data between devices that need minimal system resources. The Universal Asynchronous Receiver/Transmitter (UART) is one such standard that can realize a flexible full-duplex data exchange among different devices. The three UART controllers available on a chip are compatible with UART-enabled devices from various manufacturers. The UART can also carry out an IrDA (Infrared Data Exchange), or function as an RS-485 modem.

All UART controllers integrated in the ESP32 feature an identical set of registers for ease of programming and flexibility. In this documentation, these controllers are referred to as UARTn, where n = 0, 1, and 2, referring to UART0, UART1, and UART2, respectively.

---

### 19.2 UART Features

The UART modules have the following main features:

- Programmable baud rate
- 1024 x 8-bit RAM shared by three UART transmit-FIFOs and receive-FIFOs
- Supports input baud rate self-check
- Supports 5/6/7/8 bits of data length
- Supports 1/1.5/2 STOP bits
- Supports parity bit
- Supports RS485 Protocol
- Supports IrDA Protocol
- Supports DMA to communicate data in high speed
- Supports UART wake-up
- Supports both software and hardware flow control

---

### 19.3 Functional Description

#### 19.3.1 Introduction

UART is a character-oriented data link that can be used to achieve communication between two devices. The asynchronous mode of transmission means that it is not necessary to add clocking information to the data.

**Footer:**
Espressif Systems  
Page Number: 311  
Document Version: ESP32 TRM (Version 5.6)  
Submit Documentation Feedback