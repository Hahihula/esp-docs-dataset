

```markdown
Register 11.18. PMU_HP_MODEM_HP_SYS_CNTL_REG (0x0044)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | PMU_HP_MODEM_DIG_CPU_STALL                 |                                                                             |
| 29  | PMU_HP_MODEM_DIG_PAUSE_WDT                 |                                                                             |
| 28  | PMU_HP_MODEM_LP_PAD_SLP_SEL                |                                                                             |
| 27  | PMU_HP_MODEM_LP_PAD_HOLD_ALL                |                                                                             |
| 26  | PMU_HP_MODEM_HP_PAD_HOLD_ALL               |                                                                             |
| 25  | PMU_HP_MODEM_UART_WAKEUP_EN                | Configures whether to enable UART wake-up function in HP_MODEM state.        |
| 24  | (reserved)                                 |                                                                             |
| ... | ...                                       | ...                                                                           |
| 0   | Reset                                      | 0                                                                              |

PMU_HP_MODEM_UART_WAKEUP_EN
Configures whether to enable UART wake-up function in HP_MODEM state.
O: Disable wake-up function
1: Enable wake-up function
(R/W)

PMU_HP_MODEM_LP_PAD_HOLD_ALL
Configures whether to hold LP GPIOs' configuration in HP_MODEM state.
O: Do not hold
1: Hold
(R/W)

PMU_HP_MODEM_HP_PAD_HOLD_ALL
Configures whether to hold HP GPIOs' configuration in HP_MODEM state.
O: Do not hold
1: Hold
(R/W)

PMU_HP_MODEM_DIG_PAD_SLP_SEL
Configures whether to use Light-sleep mode configuration for GPIO in HP_MODEM state.
O: Use normal configuration
1: Use Light-sleep mode configuration. For details please refer to Chapter 6 GPIO Matrix and IO MUX > Section 6.8 Pin Functions in Light-sleep.
(R/W)

PMU_HP_MODEM_DIG_PAUSE_WDT
Configures whether to pause watchdog in HP_MODEM state.
O: Do not pause
1: Pause
(R/W)

PMU_HP_MODEM_DIG_CPU_STALL
Configures whether to stall CPU in HP_MODEM state.
O: Do not stall
1: Stall
(R/W)
```