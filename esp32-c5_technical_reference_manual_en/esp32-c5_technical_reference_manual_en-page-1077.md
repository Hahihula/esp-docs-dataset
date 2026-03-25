

```markdown
Chapter 32 UART Controller (UART)

Register 32.46. LP_UART_CONFO_SYNC_REG (0x0020)
```

Continued from the previous page...

LP_UART_TX_FLOW_EN Configures whether or not to enable flow control for the transmitter.
- O: Disable
- 1: Enable
(R/W)

LP_UART_RXD_INV Configures whether or not to invert the level of LP UART RXD signal.
- O: Not invert
- 1: Invert
(R/W)

LP_UART_TXD_INV Configures whether or not to invert the level of LP UART TXD signal.
- O: Not invert
- 1: Invert
(R/W)

LP_UART_DIS_RX_DAT_OVF Configures whether or not to disable data overflow detection for the LP UART receiver.
- O: Enable
- 1: Disable
(R/W)

LP_UART_ERR_WR_MASK Configures whether or not to store the received data with errors into FIFO.
- O: Store
- 1: Not store
(R/W)

LP_UART_MEM_CLK_EN Configures whether or not to enable clock gating for LP UART memory.
- O: Disable
- 1: Enable
(R/W)

LP_UART_SW_RTS Configures the RTS signal used in software flow control.
- O: The LP UART transmitter is not allowed to send data.
- 1: The LP UART transmitted is allowed to send data.
(R/W)

LP_UART_RXFIFO_RST Configures whether or not to reset the LP UART RX FIFO.
- O: Not reset
- 1: Reset
(R/W)

LP_UART_TXFIFO_RST Configures whether or not to reset the LP UART TX FIFO.
- O: Not reset
- 1: Reset
(R/W)
```