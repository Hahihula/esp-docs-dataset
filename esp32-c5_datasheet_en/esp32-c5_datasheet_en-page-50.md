**Title: Functional Description**

---

### **4.2 Peripherals**

This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

#### 4.2.1 Connectivity Interface

This subsection describes the connectivity interfaces on the chip that enable communication and interaction with external devices and networks.

##### 4.2.1.1 UART Controller

ESP32-C5 has three UART interfaces, i.e., UART0, UART1, and LP UART. All the three interfaces provide hardware flow control (CTS and RTS signals) and software flow control (XON and XOFF).

**Feature List**
- programmable baud rates up to 5 Mbaud
- RAM shared by TX FIFOs and RX FIFOs
- support for various lengths of data bits and stop bits
- parity bit support
- special character AT_CMD detection
- RS485 protocol support (not supported by LP UART)
- IrDA protocol support (not supported by LP UART)
- high-speed data communication using GDMA (not supported by LP UART)
- receive timeout feature
- UART as the wake-up source
- software and hardware flow control

For details, see ESP32-C5 Technical Reference Manual > Chapter UART Controller (UART).

---

### **Pin Assignment**

The pins connected to transmit and receive signals (UOTXD and UORXD) for UART0 are multiplexed with GPIO11 and GPIO12 via IO MUX. Other signals can be routed to any GPIOs via the GPIO matrix.

For LP UART, the pins used are multiplexed with LP_GPIO0 ~ LP_GPIO5 via LP IO MUX.

For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

#### **4.2.1.2 SPI Controller**

ESP32-C5 features three SPI interfaces (SPI0, SPI1, and SPI2). SPI0 and SPI1 can be configured to operate in SPI memory mode, while SPI2 can be configured to operate in general-purpose SPI mode.

Espressif Systems

Submit Documentation Feedback
ESP32-C5 Series Datasheet v1.0