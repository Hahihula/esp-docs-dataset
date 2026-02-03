**Title:**
Chapter 26 UART Controller (UART)

**Menu/Navigation Link:**
GoBack

**Table Title and Description:**
Register 26.9. UART_CONFO_REG (0x0020)

**Table Content with Descriptions for Each Register Field:**

- **UART_PARITY**: This bit is used to configure the parity check mode.
- **UART_PARITY_EN**: Set this bit to enable UART parity check.
- **UART_BIT_NUM**: This field is used to set the length of data. (R/W)
- **UART_STOP_BIT_NUM**: This field is used to set the length of stop bit. (R/W)
- **UART_SW_RTS**: This bit is used to configure the software RTS signal which is used in software flow control.
- **UART_SW_DTR**: This bit is used to configure the software DTR signal which is used in software flow control
- **UART_TXD_BRK**: Set this bit to enable the transmitter to send NULL characters when the process of sending data is done. (R/W)
- **UART_IRDA_DPLX**: Set this bit to enable IrDA loopback mode.
- **UART_IRDA_TX_EN**: This is the start enable bit for IrDA transmitter. (R/W)
- **UART_IRDA_WCTL**: 0: Set IrDA transmitter’s 11th bit to 0; 1: The IrDA transmitter's 11th bit is the same as 10th bit.
- **UART_IRDA_TX_INV**: Set this bit to invert the level of IrDA transmitter. (R/W)
- **UART_IRDA_RXINV**: Set this bit to invert the level of IrDA receiver. (R/W)
- **UART_LOOPBACK**: Set this bit to enable UART loopback test mode.
- **UART_TX_FLOW_EN**: This bit enables flow control function for transmitter, (R/W)
- **UART_IRDA_EN**: Set this bit to enable IrDA protocol
- **UART_RXFIFO_RST**: Set this bit to reset the UART RX FIFO. (R/W)
- **UART_TXFIFO_RST**: Set this bit to reset the UART TX FIFO.
- **UART_RXD_INV**: Set this bit to invert the level value of UART RXD signal, (R/W)
- **UART_CTS INV**: Set this bit to invert the level value of UART CTS signal. (R/W)
- **UART_DSR INV**: Set this bit to invert the level value of UART DSR signal.

**Footer:**
Continued on the next page...

**Company and Document Information:**
Espressif Systems
956 ESP32-S3 TRM (Version 1.7)

**Links:**
Submit Documentation Feedback