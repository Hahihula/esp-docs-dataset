**Title: Peripherals**

---

### **5 Peripherals**

#### **5.1 Peripheral Overview**
ESP32-C3FH4 integrates a rich set of peripherals including SPI, UART, I2C, I2S, remote control peripheral, LED PWM controller, TWAI® controller, USB Serial/JTAG controller, temperature sensor, SAR ADC

To learn more about on-chip components, please refer to [ESP32-C3 Series Datasheet](#) > Section Functional Description.

**Note:**
The content below is sourced from ESP32-C3 Series Datasheet. Some information may not be applicable to ESP32-C3-MINI-1 and ESP32-C3-MINI-1U as not all the IO signals are exposed on the module.
To learn more about peripheral signals, please refer to [ESP32-C3 Technical Reference Manual](#) > Section Peripheral Signal List.

---

#### **5.2 Peripheral Description**
This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

##### 5.2.1 Connectivity Interface
This subsection describes the connectivity interfaces on the chip that enable communication and interaction with external devices and networks.
- **5.2.1.1 UART Controller**

ESP32-C3 has two UART interfaces, i.e. UART0 and UART1, which support IrDA and asynchronous communication (RS232 and RS485) at a speed of up to 5 Mbps. The UART controller provides hardware flow control (CTS and RTS signals) and software flow control (XON and XOFF). Both UART interfaces connect to GDMA via UHCIO, and can be accessed by the GDMA controller or directly by the CPU.

For details, see [ESP32-C3 Technical Reference Manual](#) > Chapter UART Controller (UART, I.P. UART).

##### **Pin Assignment**
The pins connected to transmit and receive signals (UOTXD and UORXD) for UART0 are multiplexed with GPIO21 ~ GPIO20 via IO MUX. Other signals can be routed to any GPIOs via the GPIO matrix.

For more information about the pin assignment, see [ESP32-C3 Series Datasheet](#) > Section I/O Pins and ESP32-C3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.
- **5.2.1.2 SPI Controller**

ESP32-C3 has the following SPI interfaces:
- **SPI0** used by ESP32-C3’s GDMA controller and cache to access in-package or off-package flash
- **SPI1** used by the CPU to access in-package or off-package flash

---

Espressif Systems  
Page 16  

[Submit Documentation Feedback](#)