**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Header:**
Register 26.18. UART_CLK_CONF_REG (0x007B)

**Table Description for Register 26.18:**
- **Columns:** Bits, Values in Hexadecimal.
- **Rows:** 
  - `31` to `0`: Bit positions with corresponding values ranging from `0` to `1`.
  
**Register Description (UART_CLK_CONF_REG):**
- `UART_SCLK_DIV_B`: The denominator of the frequency divisor. (R/W)
- `UART_SCLK_DIV_A`: The numerator of the frequency divisor. (R/W)
- `UART_SCLK_DIV_NUM`: The integral part of the frequency divisor. (R/W)
- `UART_SCLK_SEL`: Selects UART clock source.
  - APB_CLK; RC_FAST_CLK; XTAL_CLK
- `UART_SCLK_EN`: Set this bit to enable UART TX/RX clock. (R/W)
- `UART_RST_CORE`: Write 1 and then write 0 to this bit, to reset UART TX/RX. (R/W)
- `UART_TX_SCLK_EN`: Set this bit to enable UART TX clock. (R/W)
- `UART_RX_SCLK_EN`: Set this bit to enable UART RX clock. (R/W)
- `UART_TX_RST_CORE`: Write 1 and then write 0 to this bit, to reset UART TX. (R/W)
- `UART_RX_RST_CORE`: Write 1 and then write 0 to this bit, to reset UART RX. (R/W)

**Section Header:**
Register 26.19. UART_STATUS_REG (0x001C)

**Table Description for Register 26.19:**
- **Columns:** Bits, Values in Hexadecimal.
- **Rows:** 
  - `31` to `0`: Bit positions with corresponding values ranging from `0` to `1`.

**Register Description (UART_STATUS_REG):**
- `UART_TXFIFO_CNT`: Stores the number of valid data bytes in RX FIFO. (RO)
- `UART_DSRN`: This bit represents the level of the internal UART DSR signal.
- `UART_CTSN`: This bit represents the level of the internal UART CTS signal.
- `UART_RXD`: This bit represents the level of the internal UART RXD signal.
- `UART_TXFIFO_CNT`: Stores the number of data bytes in TX FIFO. (RO)
- `UART_DTRN`: This bit represents the level of the internal UART DTR signal.
- `UART_RTSN`: This bit represents the level of the internal UART RTS signal.
- `UART_TXD`: This bit represents the level of the internal UART TXD signal.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:** 
ESP32-S3 TRM (Version 1.7)