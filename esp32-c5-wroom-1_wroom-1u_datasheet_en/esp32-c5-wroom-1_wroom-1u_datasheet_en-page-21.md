**Title: Peripherals**

---

### **5 Peripherals**

#### **5.1 Peripheral Overview**
ESP32-C5 integrates a rich set of peripherals including SPI, parallel IO interface, UART, I2C, I2S, RMT (TX/RX), pulse counter, LED PWM, USB Serial/JTAG controller, MCPWM, GDMA, CAN FD controller, SDIO slave controller, BitScrambler, event task matrix, ADC, temperature sensor, brownout detector, analog voltage comparator, as well as up to 22 GPIOs, etc.

For detailed information about module peripherals, please refer to [ESP32-C5 Series Datasheet](#) > Section Functional Description.

**Note:**
The content below is sourced from ESP32-C5 Series Datasheet. Some information may not be applicable to ESP32-C5-WROOM-1 and ESP32-C5-WROOM-1U as not all the IO signals are exposed on the module.
To learn more about peripheral signals, please refer to [ESP32-C5 Technical Reference Manual](#) > Section Peripheral Signal List.

---

#### **5.2 Peripheral Description**
This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

##### 5.2.1 Connectivity Interface
This subsection describes the connectivity interfaces on the chip that enable communication and interaction with external devices and networks.
- **5.2.1.1 UART Controller**
ESP32-C5 has three UART interfaces, i.e., UART0, UART1, and LP UART. All the three interfaces provide hardware flow control (CTS and RTS signals) and software flow control (XON and XOFF).

**Feature List:**
- programmable baud rates up to 5 Mbaud
- RAM shared by TX FIFOs and RX FIFOs
- support for various lengths of data bits and stop bits
- parity bit support
- special character AT_CMD detection
- RS485 protocol support (not supported by LP UART)
- IrDA protocol support (not supported by LP UART)
- high-speed data communication using GDMA (not supported by LP UART)
- receive timeout feature

---

**Footer:**
Espressif Systems  
21 ESP32-C5-WROOM-1 & WROOM-1U Datasheet v0.8  
[Submit Documentation Feedback](#) PRELIMINARY