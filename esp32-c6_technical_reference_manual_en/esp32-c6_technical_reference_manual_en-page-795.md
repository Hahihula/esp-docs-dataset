

```markdown
Register 27.62. LP_UART_AFIFO_STATUS_REG (0x0090)

LP_UART_TX_AFIFO_FULL Represents whether or not the APB TX asynchronous FIFO is full.
O: Not full
1: Full
(RO)

LP_UART_TX_AFIFO_EMPTY Represents whether or not the APB TX asynchronous FIFO is empty.
O: Not empty
1: Empty
(RO)

LP_UART_RX_AFIFO_FULL Represents whether or not the APB RX asynchronous FIFO is full.
O: Not full
1: Full
(RO)

LP_UART_RX_AFIFO_EMPTY Represents whether or not the APB RX asynchronous FIFO is empty.
O: Not empty
1: Empty
(RO)

Register 27.63. LP_UART_AT_CMD_PRECNT_SYNC_REG (0x0050)

LP_UART_PRE_IDLE_NUM Configures the idle time before the receiver receives the first AT_CMD.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)
```