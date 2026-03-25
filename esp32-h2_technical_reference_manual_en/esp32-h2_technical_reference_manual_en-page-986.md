

# Chapter 34

## Two-wire Automotive Interface (TWAI)

The Two-wire Automotive Interface (TWAI®) is a multi-master, multi-cast communication protocol with functions such as error detection and signaling and inbuilt message priorities and arbitration. The TWAI protocol is suited for automotive and industrial applications (see Section 34.2 for more details).

ESP32-H2 contains one TWAI controller. The controller can be connected to a TWAI bus via an external transceiver. The TWAI controller contains numerous advanced features and can be utilized in a wide range of use cases, such as automotive products, industrial automation controls, building automation, etc.

### 34.1 Features

The TWAI controller on ESP32-H2 supports the following features:

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
* Acceptance Filter (supports single and dual filter modes)
* Error detection and handling:
    * Error counters
    * Configurable error warning limit
    * Error code capture
    * Arbitration lost capture
    * Automatic transceiver standby