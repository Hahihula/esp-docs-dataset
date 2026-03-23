

```markdown
Register 12.4. PMU_HP_ACTIVE_HP_SYS_CNTL_REG (0x0010)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | PMU_HP_ACTIVE_DIG_CPU_STALL                | Configures whether to stall HP CPU in HP_ACTIVE state.                      |
| 29  | PMU_HP_ACTIVE_DIG_PAUSE_WDT                | Configures whether to pause watchdog in HP_ACTIVE state.                    |
| 28  | PMU_HP_ACTIVE_LP_PAD_SLP_SEL               | Configures whether to use Light-sleep mode configuration for GPIO in HP_ACTIVE state. |
| 27  | PMU_HP_ACTIVE_HP_PAD_HOLD_ALL              | Configures whether to hold GPIO's configuration in HP_ACTIVE state.         |
| 26  | PMU_HP_ACTIVE_LP_PAD_HOLD_ALL              | Configures whether to hold LP GPIO's configuration in HP_ACTIVE state.      |
| 25  | PMU_HP_ACTIVE_UART_WAKEUP_EN               | Configures whether to enable UART wake up function in HP_ACTIVE state.       |
| 24  | (reserved)                                 |                                                                             |
| ... | ...                                       | ...                                                                           |
| 0   | Reset                                      | All bits reset to 0.                                                         |

PMU_HP_ACTIVE_UART_WAKEUP_EN
Configures whether to enable UART wake up function in HP_ACTIVE state.
O: Disable wake-up function
1: Enable wake-up function
(R/W)

PMU_HP_ACTIVE_LP_PAD_HOLD_ALL
Configures whether to hold LP GPIO's configuration in HP_ACTIVE state.
O: Do not hold
1: Hold
(R/W)

PMU_HP_ACTIVE_HP_PAD_HOLD_ALL
Configures whether to hold GPIO's configuration in HP_ACTIVE state.
O: Do not hold
1: Hold
(R/W)

PMU_HP_ACTIVE_DIG_PAD_SLP_SEL
Configures whether to use Light-sleep mode configuration for GPIO in HP_ACTIVE state.
O: Use normal configuration
1: Use Light-sleep mode configuration. For details please refer to Chapter 7 IO MUX and GPIO Matrix (GPIO, IO MUX) > Section 7.8 Pin Functions in Light-sleep.
(R/W)

PMU_HP_ACTIVE_DIG_PAUSE_WDT
Configures whether to pause watchdog in HP_ACTIVE state.
O: Do not pause
1: Pause
(R/W)

PMU_HP_ACTIVE_DIG_CPU_STALL
Configures whether to stall HP CPU in HP_ACTIVE state.
O: Do not stall
1: Stall
(R/W)
```