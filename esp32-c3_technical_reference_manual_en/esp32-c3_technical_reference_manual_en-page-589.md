

```markdown
Register 26.29. UART_AT_CMD_POSTCNT_REG (0x0054)

UART_POST_IDLE_NUM This field is used to configure the duration time between the last AT_CMD and the next data byte, in the unit of bit time (the time it takes to transfer one bit). (R/W)


Register 26.30. UART_AT_CMD_GAPTOUT_REG (0x0058)

UART_RX_GAP_TOUT This field is used to configure the duration time between the AT_CMD characters, in the unit of bit time (the time it takes to transfer one bit). (R/W)


Register 26.31. UART_AT_CMD_CHAR_REG (0x005C)

UART_AT_CMD_CHAR This field is used to configure the content of AT_CMD character. (R/W)

UART_CHAR_NUM This field is used to configure the number of continuous AT_CMD characters received by the receiver. (R/W)
```