

# Chapter 34

## SDIO Slave Controller (SDIO)

### 34.1 Overview

The ESP32-C6 features hardware support for the Secure Digital Input/Output (SDIO) device interface that conforms to the SDIO Specification V2.00. This allows an SDIO host to access the ESP32-C6 via an SDIO bus protocol.

The SDIO host can read ESP32-C6 SDIO interface registers directly or access shared memory via the Direct Memory Access (DMA) engine, thus reducing processor's overhead while keeping high performance.

### 34.2 Features

The SDIO Slave Controller has the following features:

* Compatible with SD Physical Layer Specification V2.00 and SDIO V2.00 specifications
* Support for two IO functions (except function 0)
* Support for SPI, 1-bit SDIO, and 4-bit SDIO transfer modes
* Clock range of 0 ~ 50 MHz
* Configurable sample and drive clock edge
* Integrated and SDIO-accessible registers for information interaction
* Support for SDIO interrupt mechanism
* Automatic padding data and discarding the padded data on the SDIO bus
* Block size up to 512 bytes
* Interrupt vector between the host and slave for bidirectional interrupt
* Support DMA for data transfer
* Support for wake-up from sleep when connection is retained

### 34.3 Architecture Overview

The functional block diagram of the SDIO slave module is shown in Figure 34.3-1.