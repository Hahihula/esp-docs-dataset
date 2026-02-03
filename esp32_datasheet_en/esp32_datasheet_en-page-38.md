**Title: Functional Description**

---

### Feature List

- Programmable baud rates up to 5 Mbaud
- RAM shared by TX FIFOs and RX FIFOs
- Supports input baud rate self-check
- Support for various lengths of data bits and stop bits
- Parity bit support
- Asynchronous communication (RS232 and RS485) and IrDA support
- Supports DMA to communicate data in high speed
- Supports UART wake-up
- Supports both software and hardware flow control

For details, see [ESP32 Technical Reference Manual](#) > Chapter UART Controller.

---

### Pin Assignment

The pins for UART can be chosen from any GPIOs via the GPIO Matrix.
For more information about the pin assignment, see Section 4.10 Peripheral Pin Configurations and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

---

#### Subsection: I2C Interface (Section Title)

ESP32 has two I2C bus interfaces which can serve as I2C master or slave, depending on the user’s configuration.
##### Feature List

- Two I2C controllers: one in the main system and one in the low-power system
- Standard mode (100 Kbit/s)
- Fast mode (400 Kbit/s)
- Up to 5 MHz, yet constrained by SDA pull-up strength
- Support for 7-bit and 10-bit addressing, as well as dual address mode
- Supports continuous data transmission with disabled Serial Clock Line (SCL)
- Supports programmable digital noise filter

Users can program command registers to control I2C interfaces, so that they have more flexibility.
For details, see ESP32 Technical Reference Manual > Chapter I2C Controller.

---

### Pin Assignment for Regular I2C
For regular I2C, the pins used can be chosen from any GPIOs via the GPIO Matrix. For more information about the pin assignment, see Section 4.10 Peripheral Pin Configurations and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

---

**Footer:**
Espressif Systems
ESP32 Series Datasheet v5.2

Submit Documentation Feedback