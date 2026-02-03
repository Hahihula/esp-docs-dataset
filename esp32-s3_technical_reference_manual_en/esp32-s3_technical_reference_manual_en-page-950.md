**Title:**
Chapter 26 UART Controller (UART)

**Menu/Navigation Link:**
GoBack

**Table Description with Labels and Values for Register 0x0008:**

- **Register Name:** UART_INT_ST_REG (0x0008)
- The table lists various interrupt status bits associated with different UART functions, each labeled as follows:
  - `UART_WAKE_UP_INT`
  - `UART_QMChar_DET_INT`
  - `UART_DET_ERR_INT`
  - `UART_DET_DONE_INT`
  - `UART_TXDone_INT`
  - `UART_RXDone_INT`
  - `UART_BRK_DET_INT`
  - `UART_XON_INT`
  - `UART_XOFF_INT`
  - `UART_DSR_DET_INT`
  - `UART_OVFF_DET_INT`
  - `UART_FRM_ERR_DET_INT`
  - `UART_TXFIFO_EMPTY_INT`
  - `UART_RXFIFO_FULL_INT`
  - `UART_TXFIFO_OVF_INT`
  - `UART_RXFIFO_OVF_INT`
  - `UART_DSR_CHG_INT`
  - `UART_CTS_CHG_INT`
  - `UART_BRK_DET_INT`
  - `UART_TXBRK_DET_INT`
  - `UART_TOUT_INT`
  - `UART_SW_XON_INT`
  - `UART_SW_XOFF_INT`
  - `UART_GLITCH_DET_INT`
  - `UART_TXBRK_DONE_INT`

**Descriptions:**
Each interrupt status bit is described with the following format:
- "This is the status bit for [Interrupt Name] when [Condition]."
- Conditions include setting specific bits to a certain value (e.g., set to 1).

**Example Entries from Table:**
- `UART_RXFIFO_FULL_INT` - This is the status bit for UART_RXFIFO_FULL_INT when UART_RXFIFO_FULL_ENA is set to 1. (RO)
- `UART_TXFIFO_EMPTY_INT` - This is the status bit for UART_TXFIFO_EMPTY_INT when UART_TXFIFO_EMPTY_ENA is set to 1. (RO)

**Footer:**
Continued on the next page...

**Company and Document Information at Bottom of Page:**
Espressif Systems
950 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback