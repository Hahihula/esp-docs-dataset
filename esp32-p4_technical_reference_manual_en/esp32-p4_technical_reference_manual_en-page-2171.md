

```markdown
Chapter 42 UART Controller (UART)

Register 42.61. LP_UART_AFIFO_STATUS_REG (0x0090)
```

| Bit | Description |
|-----|-------------|
| 3   | Reserved    |
| 2   | LP_UART_RX_AFIFO_EMPTY |
| 1   | LP_UART_TX_AFIFO_FULL |
| 0   | LP_UART_RX_AFIFO_FULL |

LP_UART_TX_AFIFO_FULL Represents whether or not the APB TX asynchronous FIFO is full.
- O: Not full
- 1: Full (RO)

LP_UART_TX_AFIFO_EMPTY Represents whether or not the APB TX asynchronous FIFO is empty.
- O: Not empty
- 1: Empty (RO)

LP_UART_RX_AFIFO_FULL Represents whether or not the APB RX asynchronous FIFO is full.
- O: Not full
- 1: Full (RO)

LP_UART_RX_AFIFO_EMPTY Represents whether or not the APB RX asynchronous FIFO is empty.
- O: Not empty
- 1: Empty (RO)

Register 42.62. LP_UART_AT_CMD_PRECNT_SYNC_REG (0x0050)
```

| Bit | Description |
|-----|-------------|
| 31  | Reserved    |
| 16  | LP_UART_PRE_IDLE_NUM |

LP_UART_PRE_IDLE_NUM Configures the idle time before the receiver receives the first AT_CMD.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)
```