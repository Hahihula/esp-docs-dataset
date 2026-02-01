**Title: Functional Description**

---

### **4.2 Peripherals**

This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

#### 4.2.1 Connectivity Interface

This subsection describes the connectivity interfaces on the chip that enable communication and interaction with external devices and networks.

##### 4.2.1.1 UART Controller

The UART Controller in the ESP32-C6 chip facilitates the transmission and reception of asynchronous serial data between the chip and external UART devices. It consists of two UARTs in the main system, and one low-power LP UART.

**Feature List**
- Programmable baud rates up to 5 Mbaud
- RAM shared by TX FIFOs and RX FIFOs
- Support for various lengths of data bits and stop bits
- Parity bit support
- Special character AT_CMD detection
- RS485 protocol support (not supported by LP UART)
- IrDA protocol support (not supported by LP UART)
- High-speed data communication using GDMA (not supported by LP UART)
- Receive timeout feature
- UART as the wake-up source
- Software and hardware flow control

For details, see ESP32-C6 Technical Reference Manual > Chapter UART Controller (UART, LP_UART).

---

### **Pin Assignment**

For details, see Section 2.3.5 Peripheral Pin Assignment.

#### 4.2.1.2 SPI Controller

ESP32-C6 has the following SPI interfaces:

- **SPI0** used by ESP32-C6's cache and GDMA to access in-package or off-package flash
- **SPI1** used by the CPU to access in-package or off-package flash
- **SPI2** is a general-purpose SPI controller with access to general-purpose DMA channels

SPI0 and SPI1 are reserved for system use, and only SPI2 is available for users.

---

Espressif Systems  
50  
Submit Documentation Feedback  
ESP32-C6 Series Datasheet v1.4