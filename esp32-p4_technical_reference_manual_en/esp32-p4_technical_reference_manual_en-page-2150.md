

```markdown
Register 42.27. UART_AT_CMD_POSTCNT_SYNC_REG (0x0054)

UART_POST_IDLE_NUM Configures the interval between the last AT_CMD and subsequent data.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)
```

```markdown
Register 42.28. UART_AT_CMD_GAPTOUT_SYNC_REG (0x0058)

UART_RX_GAP_TOUT Configures the interval between two AT_CMD characters.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)
```

```markdown
Register 42.29. UART_AT_CMD_CHAR_SYNC_REG (0x005C)

UART_AT_CMD_CHAR Configures the AT_CMD character. (R/W)
UART_CHAR_NUM Configures the number of continuous AT_CMD characters a receiver can receive.
(R/W)
```