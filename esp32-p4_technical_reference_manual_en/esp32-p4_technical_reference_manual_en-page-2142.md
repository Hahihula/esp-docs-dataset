

```markdown
Register 42.11. UART_HWFC_CONF_SYNC_REG (0x002C)

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)        |                                                                             |
| 9   | UART_RX_FLOW_EN    | Configures whether or not to enable the UART receiver.<br>0: Disable<br>1: Enable (R/W) |
| 8   | UART_RX_FLOW_THRD | Configures the maximum number of data bytes that can be received during hardware flow control. Measurement unit: byte. (R/W) |

Register 42.12. UART_SLEEP_CONFO_REG (0x0030)

| Bit Range | Field Name         | Description |
|-----------|--------------------|-------------|
| 31-24     | UART_WK_CHAR4      | Configures wakeup character 4. (R/W) |
| 23-16     | UART_WK_CHAR3      | Configures wakeup character 3. (R/W) |
| 15-8      | UART_WK_CHAR2      | Configures wakeup character 2. (R/W) |
| 7-0       | UART_WK_CHAR1      | Configures wakeup character 1. (R/W) |

Register 42.13. UART_SLEEP_CONF1_REG (0x0034)

| Bit | Field Name     | Description |
|-----|----------------|-------------|
| 31  | (reserved)    |             |
| 7   | UART_WK_CHARO | Configures wakeup character 0. (R/W) |
```