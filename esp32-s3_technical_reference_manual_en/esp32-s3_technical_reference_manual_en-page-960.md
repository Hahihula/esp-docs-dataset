**Chapter Title:**
Chapter 26 UART Controller (UART)

**GoBack Link:** GoBack

---

### Register Section:

#### Register 26.16. UART_IDLE_CONFIG_REG (0x0048)
- **Field Description:**
  - `UART_RX_IDLE_THRHD`: A frame end signal is generated when the receiver takes more time to receive one byte data than the value of this field, in unit bit time.
  - `UART_TX_IDLE_NUM`: This field is used to configure the duration time between transfers.

#### Register 26.17. UART_RS485_CONFIG_REG (0x004C)
- **Field Description:**
  - `UART_RS485_EN`: Set this bit to choose RS485 mode.
  - `UART_DLO_EN`: Configures whether or not to add a turnaround delay of 1 bit before the start bit. Options are:
    - `0`: Not add
    - `1`: Add (R/W)
  - `UART_DL1_EN`: Configures whether or not to add a turnaround delay of 1 bit after the stop bit.
    - `0`: Not add
    - `1`: Add (R/W)
  - `UART_RS485_TX_RX_EN`: Set this bit to enable receiver could receive data when the transmitter is transmitting data in RS485 mode. Options are:
    - `1`: enable RS485 transmitter to send data when RS485 receiver line is busy.
  - `UART_RS485_RX_BY_TX_EN`: This field used to delay the receiver’s internal data signal (R/W).
  - `UART_RS485_TX_DLY_NUM` and `UART_RS485_TX_DLY_NUM`: These fields are for delaying signals.

---

**Footer:**
Espressif Systems
960 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback