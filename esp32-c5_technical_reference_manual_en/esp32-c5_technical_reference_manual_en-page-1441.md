

# Chapter 39

## SDIO Slave Controller (SDIO)

### 39.1 Overview

The ESP32-C5 features hardware support for the Secure Digital Input/Output (SDIO) device interface that conforms to the SDIO Specification V2.00. This interface allows an SDIO host to access the ESP32-C5 using the SDIO bus protocol.

The SDIO host can directly access the ESP32-C5 SDIO interface registers or use the Direct Memory Access (DMA) engine to access shared memory. This approach reduces processor overhead and maintains high performance.

### 39.2 Features

The SDIO Slave Controller has the following features:

- Compatible with SD Physical Layer Specification V2.00 and SDIO V2.00 specifications
- Support for two I/O functions (excluding function 0)
- Support for SPI, 1-bit SDIO, and 4-bit SDIO transfer modes
- Clock frequency range from 0 to 50 MHz
- Configurable sample and drive clock edge
- Integrated and SDIO-accessible registers for information exchange
- Support for SDIO interrupt mechanism
- Automatic padding data and discarding the padded data on the SDIO bus
- Block size up to 512 bytes
- Bidirectional interrupt vector between host and slave
- DMA support for data transfer
- Wake-up from sleep mode when connection is retained

**Note:**
The SDIO Slave controller can be used together with the USB Serial/JTAG controller in 1-bit SDIO transfer mode, but not in 4-bit SDIO transfer mode.