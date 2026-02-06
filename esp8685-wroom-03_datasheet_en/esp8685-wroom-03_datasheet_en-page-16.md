**Title: Peripherals**

---

### **5 Peripherals**

#### **5.1 Peripheral Overview**
ESP8685H4 integrates a rich set of peripherals including SPI, I2S, UART, I2C, RMT, LED PWM controller, TWAI® controller, USB Serial/JTAG controller, temperature sensor, etc.

To learn more about on-chip components, please refer to [ESP8685 Series Datasheet](#) > Section Functional Description.

---

**Note:**
The content below is sourced from ESP8685 Series Datasheet > Section Peripherals. Some information may not be applicable to ESP8685-WROOM-03 as not all the IO signals are exposed on the module.
To learn more about peripheral signals, please refer to [ESP32-C3 Technical Reference Manual](#) > Section Peripheral Signal List.

---

#### **5.2 Peripheral Description**
This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

##### 5.2.1 Connectivity Interface
This subsection describes the connectivity interfaces on the chip that enable communication and interaction with external devices and networks.

###### 5.2.1.1 UART Controller

ESP8685 has two UART interfaces, i.e., UART0 and UART1, which support IrDA and asynchronous communication (RS232 and RS485) at a speed of up to 5 Mbps. The UART controller provides hardware flow control (CTS and RTS signals) and software flow control (XON and XOFF). Both UART interfaces connect to GDMA via UHClO, and can be accessed by the GDMA controller or directly by the CPU.

**Pin Assignment**
For details, see [ESP8685 Series Datasheet](#) > Section Peripheral Pin Assignment.

---

##### 5.2.1.2 SPI Controller

ESP8685 has the following SPI interfaces:

- **SPI0**: used by ESP8685’s GDMA controller and cache to access in-package flash
- **SPI1**: used by the CPU to access in-package flash
- **SPI2**: is a general purpose SPI controller with access to a DMA channel allocated by the GDMA controller

---

**Features of SPI0 and SPI1**
- Supports Single SPI, Dual SPI, and Quad SPI, QPI modes

---

Espressif Systems  
[Submit Documentation Feedback](#) ESP8685-WROOM-03 Datasheet v1.5