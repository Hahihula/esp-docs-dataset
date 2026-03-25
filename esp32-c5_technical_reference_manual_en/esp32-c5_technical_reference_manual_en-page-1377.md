

# Chapter 38

## Controller Area Network Flexible Data-Rate (CAN FD)

The CAN FD is a multi-master multi-cast communication protocol with error detection and signaling and built-in message priorities and arbitration. It implements the CAN protocol as specified by ISO11898-1. The CAN protocol is suitable for automotive and industrial applications.

### 38.1 Overview

ESP32-C5 contains two CAN FD controllers that can be connected to a CAN FD bus via an external transceiver. The CAN FD contains numerous advanced features and can be utilized in a wide range of use cases such as automotive products, industrial automation controls, building automation, etc.

This chapter provides functional description of CAN FD, programmer models and parameters of CAN FD. It is intended to be used as a reference for software driver developers.

### 38.2 Feature List

The CAN FD of ESP32-C5 has the following features:

- Compliant with ISO11898-1:2015
- RX FIFO with 128 words (6 CAN FD frames with 64 byte of payload)
- 4 TX buffers (1 CAN FD frame in each TX buffer)
- 32-bit APB interface
- Support of ISO and non-ISO CAN FD protocols
- Timestamping and time triggered transmission
- Interrupt-driven operation
- Three single-bit filters and one range filter
- Loopback, bus monitoring, ACK forbidden, self test, and restricted operation modes

### 38.3 Functional Description

#### 38.3.1 Clock

CAN FD operates with a single clock, which is TWAI_CLK. All timing parameters are derived from the clock.