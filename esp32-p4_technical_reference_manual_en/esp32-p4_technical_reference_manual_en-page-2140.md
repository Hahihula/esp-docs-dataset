

```markdown
Register 42.9. UART_CONFO_SYNC_REG (0x0020)
```

Continued from the previous page...

UART_ERR_WR_MASK Configures whether or not to store the received data with errors into FIFO.
- O: Store
- 1: Not store
(R/W)

UART_AUTBAUD_EN Configures whether or not to enable baud rate detection.
- O: Disable
- 1: Enable
(R/W)

UART_MEM_CLK_EN Configures whether or not to enable clock gating for UART memory.
- O: Disable
- 1: Enable
(R/W)

UART_SW_RTS Configures the RTS signal used in software flow control.
- O: The UART transmitter is not allowed to send data.
- 1: The UART transmitted is allowed to send data.
(R/W)

UART_RXFIFO_RST Configures whether or not to reset the UART RX FIFO.
- O: Not reset
- 1: Reset
(R/W)

UART_TXFIFO_RST Configures whether or not to reset the UART TX FIFO.
- O: Not reset
- 1: Reset
(R/W)
```