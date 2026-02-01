**Title:**
2 Pins

**Subtitle and Section Heading:**
2.3.2 LP IO MUX Functions

**Body Text:**
When the chip is in Deep-sleep mode, the IO MUX described in Section 2.3.1 IO MUX Pin Functions will not work. That is where the LP IO MUX comes in. It allows multiple input/output signals to be a single input/output pin in Deep-sleep mode, as the pin is connected to the LP system and powered by VDDPST1.

LP IO pins can be assigned to LP functions. They can:
- Either work as LP GPIOs (LP_GPIO0, LP_GPIO1, etc.), connected to the LP CPU
- Or connect to LP peripheral signals (LP_I2C_SDA, LP_I2C_SCL, etc.) - see Table 2-6 LP Peripheral Signals Routed via LP IO MUX

**Table:**
- **Title:** Table 2-6. LP Peripheral Signals Routed via LP IO MUX
- **Columns:** Pin Function | Signal | Description
- **Rows:**
  - [LP_I2C_SDA](#) | Serial data | LP I2C interface
  - [LP_I2C_SCL](#) | Serial clock | Sclial clock
  - [LP_UART_RXD](#) | Receive | Receive
  - [LP_UART_TXD](#) | Transmit | Transmit
  - [LP_UART_RTSN](#) | Request to send | Request to send
  - [LP_UART_CTSN](#) | Clear to send | Clear to send
  - [LP_UART_DTRN](#) | Data set ready | Data set ready
  - [LP_UART_DSRN](#) | Data terminal ready | Data terminal ready

**Table:**
- **Title:** Table 2-7. LP IO MUX Functions shows the LP functions of LP IO pins.
- **Columns:** No., LP IO Name, F0, F1
- **Rows:**
  - [6](#) | LP_GPIO0 | LP_GPIO0 | LP_UART_DTRN
  - [7](#) | LP_GPIO1 | LP_GPIO1 | LP_UART_SRSN
  - [8](#) | LP_GPIO2 | LP_GPIO2 | LP_UART_RTSN
  - [9](#) | LP_GPIO3 | LP_GPIO3 | LP_UART_CTSN
  - [10](#) | LP_GPIO4 | LP_GPIO4 | LP_UART_RXD
  - [11](#) | LP_GPIO5 | LP_GPIO5 | LP_UART_TXD
  - [12](#) | LP_GPIO6 | LP_GPIO6 | LP_I2C_SDA
  - [13](#) | LP_GPIO7 | LP_GPIO7 | LP_I2C_SCL

**Additional Information:**
- **Bold marks the default pin functions in the default boot mode. See Section 3.1 Chip Boot Mode Control.**
- This column lists the LP GPIO names, since LP functions are configured with LP GPIO registers that use LP GPIO numbering.
- Regarding highlighted cells, see Section 2.3.4 Restrictions for GPIOs and LP GPIOs.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number:** 
22  
**Document Version:** ESP32-C6 Series Datasheet v1.4