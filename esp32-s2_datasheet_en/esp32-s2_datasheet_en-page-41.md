**Title: Functional Description**

- **GPIO35 = IO6**
- **GPIO36 = IO7**
- **GPIO37 = DQS**

**SPI 4-line mode:**
- SPID (SPID) = IO0
- SPIQ (SPIQ) = IO1
- SPIWP (SPIWP) = IO2
- SPIHD (SPIHD) = IO3

**SPI 2-line mode:**
- SPID (SPID) = IO0
- SPIQ (SPIQ) = IO1

**SPI 1-line mode:**
- SPID (SPID) = DI
- SPIQ (SPIQ) = DO
- SPIWP (SPIWP) = WP#
- SPIHD (SPIHD) = HOLD#

For more information, please refer to [ESP32-S2 Technical Reference Manual > Chapter SPI Controller (SPI)](#).

**Pin Assignment**

For details, see Section 2.3.6 Peripheral Pin Assignment.

---

**Title: LCD Controller**
**Subtitle: 4.2.1.3**

SPI2 supports parallel 8-bit RGB, I8080 and Moto6800 interfaces. I2S supports 8/16/24-bit parallel interface (8080).

For more information, please refer to [ESP32-S2 Technical Reference Manual > Chapter SPI Controller (SPI)](#) and [ESP32-S2 Technical Reference Manual > Chapter I2S Controller (I2S)](#).

**Pin Assignment**

For details, see Section 2.3.6 Peripheral Pin Assignment.

---

**Title: UART Controller**
**Subtitle: 4.2.1.4**

ESP32-S2 has two UART interfaces, i.e., UART0, UART1, which provide asynchronous communication (RS232 and RS485) and IrDA support, communicating at a speed of up to 5 Mbps. UART provides hardware management of the CTS and RTS signals and software flow control (XON and XOFF). All of the interfaces can be accessed by the DMA controller or directly by the CPU.

---

**Footer:**
- Espressif Systems
- Page number: 41
- Document title: ESP32-S2 Series Datasheet v1.8

[Submit Documentation Feedback](#)