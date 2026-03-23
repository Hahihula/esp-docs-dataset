

```markdown
Register 26.32. UART_DATE_REG (0x007C)

UART_DATE    This is the version control register. (R/W)


Register 26.33. UART_ID_REG (0x0080)

UART_ID      This field is used to configure the UART_ID. (R/W)

UART_UPDATE_CTRL   This bit is used to control register synchronization mode. This bit must be cleared before writing 1 to UART_REG_UPDATE to synchronize configured values to UART Core’s clock domain. (R/W)

UART_REG_UPDATE    When this bit is set to 1 by software, registers are synchronized to UART Core’s clock domain. This bit is cleared by hardware after synchronization is done. (R/W/SC)
```