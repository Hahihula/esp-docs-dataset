**Title: Peripherals**

---

### **5.1 Peripheral Overview**

ESP32-C61 integrates a rich set of peripherals including GPIO, SPI, UART, I2C, I2S, LED PWM, USB Serial/JTAG controller, GDMA, On-chip debug functionality via JTAG, event task matrix, ADC, temperature sensor, brown-out detector, analog voltage comparator, general-purpose timers, system timer, and watchdog timers etc.

To learn more about on-chip components, please refer to [ESP32-C61 Series Datasheet](#) > Section Functional Description.

**Note:**
The content below is sourced from ESP32-C61 Series Datasheet > Section Peripherals. Some information may not be applicable to ESP32-C61-MINI-1 and ESP32-C61-MINI-1U as not all the IO signals are exposed on the module.
To learn more about peripheral signals, please refer to [ESP32-C61 Technical Reference Manual](#) > Section Peripheral Signal List.

---

### **5.2 Peripheral Description**

This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

#### 5.2.1 Connectivity Interface

This subsection describes the connectivity interfaces on the chip that enable communication and interaction with external devices and networks.

##### 5.2.1.1 UART Controller

The UART Controller in the ESP32-C61 chip facilitates the transmission and reception of asynchronous serial data between the chip and external UART devices. It supports three UART interfaces.

**Feature List**
- Programmable baud rates up to 5 Mbaud
- RAM shared by TX FIFOs and RX FIFOs
- Support for various lengths of data bits and stop bits
- Parity bit support
- Special character AT_CMD detection
- RS485 protocol support
- IrDA protocol support
- High-speed data communication using GDMA
- Receive timeout feature

---

**Footer:**
Espressif Systems  
[Submit Documentation Feedback](#) ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6