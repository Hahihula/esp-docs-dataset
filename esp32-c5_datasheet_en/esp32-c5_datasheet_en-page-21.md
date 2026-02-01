**Title:**
2 Pins

**Subtitle:**
2.3.2 LP IO MUX Functions

**Body Text:**
When the chip is in Deep-sleep mode, the IO MUX described in Section 2.3.1 IO MUX Functions will not work.
That is where the LP IO MUX comes in. It allows multiple input/output signals to be a single input/output pin in Deep-sleep mode, as the pin is connected to the LP system and powered by VDDPST1.

LP IO pins can be assigned to LP functions. They can:
- Either work as LP GPIOs (LP_GPIO0, LP_GPIO1, etc.), connected to the LP CPU
- Or connect to LP peripheral signals (LP_I2C_SDA, LP_I2C_SCL, etc.) - see Table 2-4 LP Peripheral Signals Routed via LP IO MUX

**Table:**
- **Title:** Table 2-4. LP Peripheral Signals Routed via LP IO MUX
- | Pin Function | Signal | Description |
| --- | --- | --- |
| LP_I2C_SDA | Serial data | LP I2C interface |
| LP_I2C_SCL | Serial clock | Receive |
| LP_UART_RXD | Transmit | Data terminal ready |
| LP_UART_TXD | Request to send | Clear to send |
| LP_UART_RTSN |  | LP UART interface |
| LP_UART_CTSN |  | Set data set ready |

**Table:**
- **Title:** Table 2-5. LP IO MUX Functions
- Pin No.
   - F0
   - F1
   - F2
   - F3

| Pin No. | Name | LP IOMUX Function |
| --- | --- | --- |
| 9 | LP_GPIO0 | LP_UART_DTRN | LP_GPIO0 |
| 10 | LP_GPIO7 | LP_UART_DSRN | LP_GPIO1 |
| 11 | LP_GPIO2 | LP_UART_RTSN^2 | LP_GPIO2 | LP_I2C_SDA^2 |
| 12 | LP_GPIO3 | LP_UART_CTSN | LP_GPIO3 | LP_I2C_SCL |
| 13 | LP_GPIO4 | LP_UART_RXD | LP_GPIO4 |
| 14 | LP_GPIO5 | LP_UART_TXD | LP_GPIO5 |
| 15 | LP_GPIO6 | LP_UART_GIO6 | LP_GPIO6 |

**Footnotes:**
^2 This column lists the LP GPIO names, since LP functions are configured with LP GPIO registers that use LP GPIO numbering.
^3 Hardware flow control of LP_UART cannot be used with LP_I2C at the same time.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version:** ESP32-C5 Series Datasheet v1.0