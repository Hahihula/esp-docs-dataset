

# Chapter 53

## Two-Wire Automotive Interface (TWAI)

The Two-wire Automotive Interface (TWAI®) is a multi-master, multi-cast communication protocol with functions such as error detection and signaling and inbuilt message priorities and arbitration. The TWAI protocol is suited for automotive and industrial applications (see Section 53.2 for more details).

ESP32-P4 contains three TWAI controllers, TWAI 0, TWAI 1, and TWAI 2. Each controller can individually be connected to a TWAI bus via an external transceiver. The TWAI controllers have many advanced features, and can be utilized in a wide range of use cases, such as automotive products, industrial automation controls, building automation, etc.

### 53.1 Features

Each TWAI controller on ESP32-P4 supports the following features:

* Compatibility with ISO 11898-1 protocol (CAN Specification 2.0)
* Standard Frame Format (11-bit ID) and Extended Frame Format (29-bit ID)
* Bit rates from 1 Kbit/s to 1 Mbit/s
* Multiple modes of operation:
    * Normal
    * Listen-only (no influence on bus)
    * Self-test (no acknowledgment required during data transmission)
* 64-byte Receive FIFO
* Special transmissions:
    * Single-shot transmissions (does not automatically re-transmit upon error)
    * Self-reception (the TWAI controller transmits and receives messages simultaneously)
* Acceptance Filter (supports Single and Dual-filter modes)
* Error detection and handling:
    * Error counters
    * Configurable error warning limit
    * Error code capture
    * Arbitration lost capture
    * Automatic transceiver standby