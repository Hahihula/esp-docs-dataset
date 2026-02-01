**Title: Functional Description**

---

### Feature List

- Compatible with ISO 11898-1 protocol (CAN Specification 2.0)
- Standard frame format (11-bit ID) and extended frame format (29-bit ID)
- Bit rates from 1 Kbit/s to 1 Mbit/s
- Multiple modes of operation: Normal, Listen Only, and Self-Test (no acknowledgment required)
- Special transmissions: Single-shot and Self Reception
- Acceptance filter (single and dual filter modes)
- Error detection and handling: error counters, configurable error warning limit, error code capture, arbitration lost capture, automatic transceiver standby

For details, see [ESP32-C6 Technical Reference Manual > Chapter Two-wire Automotive Interface](#).

---

### Pin Assignment

For details, see Section 2.3.5 Peripheral Pin Assignment.

---

**Title: SDIO Slave Controller**

### Subtitle: 4.2.1.8 SDIO Slave Controller

The SDIO Slave Controller in the ESP32-C6 chip provides hardware support for the Secure Digital Input/Output (SDIO) device interface. It allows an SDIO host to access the ESP32-C6 via an SDIO bus protocol.

---

### Feature List

- Compatible with SD Physical Layer Specification V2.00 and SDIO V2.00 specifications
- Support for SPI, 1-bit SDIO, and 4-bit SDIO transfer modes
- Clock range of 0 ~ 50 MHz
- Configurable sample and drive clock edge
- Integrated and SDIO-accessible registers for information interaction
- Support for SDIO interrupt mechanism
- Automatic padding data and discarding the padded data on the SDIO bus
- Block size up to 512 bytes
- Interrupt vector between the host and slave for bidirectional interrupt
- Support DMA for data transfer
- Support for wake-up from sleep when connection is retained

For more details about the SDIO Slave Controller, refer to the [ESP32-C6 Technical Reference Manual > Chapter SDIO Slave Controller (SDIO)](#).

---

### Pin Assignment

For details, see Section 2.3.5 Peripheral Pin Assignment.

---

**Footer:**

Espressif Systems  
[Submit Documentation Feedback](#)  

Page number: **54**  
Document version: ESP32-C6 Series Datasheet v1.4