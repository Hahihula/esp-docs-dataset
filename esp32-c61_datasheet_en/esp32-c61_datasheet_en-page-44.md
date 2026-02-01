**Title: Functional Description**

---

### **4.2 Peripherals**

This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

#### 4.2.1 Connectivity Interface

This subsection describes the connectivity interfaces on the chip that enable communication and interaction with external devices and networks.

##### 4.2.1.1 UART Controller

The UART Controller in the ESP32-C61 chip facilitates the transmission and reception of asynchronous serial data between the chip and external UART devices. It supports three UART interfaces.

**Feature List:**
- Programmable baud rates up to 5 Mbaud
- RAM shared by TX FIFOs and RX FIFOs
- Support for various lengths of data bits and stop bits
- Parity bit support
- Special character AT_CMD detection
- RS485 protocol support
- IrDA protocol support
- High-speed data communication using GDMA
- Receive timeout feature
- UART as the wake-up source
- Software and hardware flow control

**Pin Assignment:**
The pins connected to transmit and receive signals (UOTXD and UORXD) for UART0 are multiplexed with GPIO10 ~ GPIO11 via IO MUX. Other signals can be routed to any GPIOs via the GPIO matrix.

#### 4.2.1.2 SPI Controller

ESP32-C61 has the following SPI interfaces:

- **SPI0** used by ESP32-C61's cache and GDMA to access in-package or off-package flash/PSRAM
- **SPI1** used by the CPU to access in-package or off-package flash/PSRAM
- **SPI2** is a general-purpose SPI controller with access to general-purpose DMA channels

SPI0 and SPI1 are reserved for system use, and only SPI2 is available for users.

---

Espressif Systems  
44 ESP32-C61 Series Datasheet v0.5