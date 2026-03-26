

```markdown
## Register 42.63. LP_UART_AT_CMD_POSTCNT_SYNC_REG (0x0054)

LP_UART_POST_IDLE_NUM Configures the interval between the last AT_CMD and subsequent data.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)


## Register 42.64. LP_UART_AT_CMD_GAPTOUT_SYNC_REG (0x0058)

LP_UART_RX_GAP_TOUT Configures the interval between two AT_CMD characters.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)


## Register 42.65. LP_UART_AT_CMD_CHAR_SYNC_REG (0x005C)

LP_UART_AT_CMD_CHAR Configures the AT_CMD character. (R/W)
LP_UART_CHAR_NUM Configures the number of continuous AT_CMD characters a receiver can receive. (R/W)
```