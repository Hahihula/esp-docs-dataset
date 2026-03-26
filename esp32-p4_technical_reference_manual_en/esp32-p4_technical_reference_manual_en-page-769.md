

```markdown
Register 10.76. LPPERI_MEM_CTRL_REG (0x0028)

| Bit | Field Description                  |
|-----|------------------------------------|
| 31  | LPPEIR_LP_UART_WAKEUP_FLAG_CLR    |
| 30  | LPPEIR_LP_UART_WAKEUP_FLAG        |
| 29  | LPPEIR_LP_UART_WAKEUP_EN          |
| 28  | LPPEIR_LP_UART_MEM_FORCE_PD       |
| 27  | LPPEIR_LP_UART_MEM_FORCE_PU       |
| ... | (reserved)                        |
| 1   | [Reserved]                        |
| 0   | Reset                              |

LPPEIR_LP_UART_WAKEUP_FLAG_CLR Write 1 to clear LPPEIR_LP_UART_WAKEUP_FLAG. (WT)

LPPEIR_LP_UART_WAKEUP_FLAG Represents whether an LP UART wakeup has occurred.
- O: No LP UART wakeup occurred
- 1: LP UART wakeup occurred (R/WTC/SS)

LPPEIR_LP_UART_WAKEUP_EN Configures whether to enable the LP UART wakeup function.
- O: Enable
- 1: Disable (R/W)

LPPEIR_LP_UART_MEM_FORCE_PD Configures whether to force the LP UART memory to power down.
- O: Do not force power down
- 1: Force power down (R/W)

LPPEIR_LP_UART_MEM_FORCE_PU Configures whether to force the LP UART memory to power up.
- O: Do not force power up
- 1: Force power up (R/W)
```