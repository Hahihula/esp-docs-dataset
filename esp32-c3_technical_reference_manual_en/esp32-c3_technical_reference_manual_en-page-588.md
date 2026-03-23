

```markdown
Register 26.26. UART_POSPULSE_REG (0x0070)

UART_POSEDGE_MIN_CNT This field stores the minimal input clock count between two positive edges. It is used in baud rate detection. (RO)


Register 26.27. UART_NEGPULSE_REG (0x0074)

UART_NEGEDGE_MIN_CNT This field stores the minimal input clock count between two negative edges. It is used in baud rate detection. (RO)


Register 26.28. UART_AT_CMD_PRECNT_REG (0x0050)

UART_PRE_IDLE_NUM This field is used to configure the idle duration time before the first AT_CMD is received by the receiver, in the unit of bit time (the time it takes to transfer one bit). (R/W)
```