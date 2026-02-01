**Title: Functional Description**

---

### **4.2 Peripherals**

This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

#### 4.2.1 Connectivity Interfaces

This subsection describes the connectivity interfaces on the chip that enable communication and interaction with external devices and networks.

##### 4.2.1.1 UART Controller

The UART Controller in the ESP32-H2 chip facilitates the transmission and reception of asynchronous serial data between the chip and external UART devices. It consists of two UARTs in the system.

**Feature List:**
- Programmable baud rates up to 5 Mbaud
- 260 x 8 bit RAM shared by TX FIFOs and RX FIFOs
- Support for various lengths of data bits and stop bits
- Parity bit support
- Special character AT_CMD detection
- RS485 protocol support
- IrDA protocol support
- High-speed data communication using GDMA
- Receive timeout feature
- UART as the wake-up source
- Software and hardware flow control

For details, see [ESP32-H2 Technical Reference Manual > Chapter UART Controller (UART)](#).

---

### **Pin Assignment**

The pins connected to receive and transmit signals (UORXD and UOTXD) for UART0 are multiplexed with GPIO23 ~ GPIO24 and FSPICS1 ~ FSPICS2 via IO MUX. Other signals can be routed to any GPIOs via the GPIO matrix.

For more information about the pin assignment, see Section 2.3 IO Pins in [ESP32-H2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](#).

---

### **4.2.1.2 SPI Controller**

ESP32-H2 has the following SPI interfaces:

- **SPI0/SPI1** are reserved for system use.
- **SPI2** is a general-purpose SPI (GP-SPI) controller with access to general-purpose DMA channels.

Espressif Systems

---

[Submit Documentation Feedback](#)

40
ESP32-H2 Series Datasheet v1.2