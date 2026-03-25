

```markdown
Register 13.24. PMU_HP_SLEEP_HP_SYS_CNTL_REG (0x0078)

PMU_HP_SLEEP_UART_WAKEUP_EN Configures whether to enable UART wake up function in HP_SLEEP state.
O: Disable wake-up function
1: Enable wake-up function
(R/W)

PMU_HP_SLEEP_LP_PAD_HOLD_ALL Configures whether to hold LP GPIO's configuration in HP_SLEEP state.
O: Do not hold
1: Hold
(R/W)

PMU_HP_SLEEP_HP_PAD_HOLD_ALL Configures whether to hold GPIO's configuration in HP_SLEEP state.
O: Do not hold
1: Hold
(R/W)

PMU_HP_SLEEP_DIG_PAD_SLP_SEL Configures whether to use Light-sleep mode configuration for GPIO in HP_SLEEP state.
O: Use normal configuration
1: Use Light-sleep mode configuration. For details please refer to Chapter 8 GPIO Matrix and IO MUX > Section 8.8 Pin Functions in Light-sleep.
(R/W)

PMU_HP_SLEEP_DIG_PAUSE_WDT Configures whether to pause watchdog in HP_SLEEP state.
O: Do not pause
1: Pause
(R/W)

PMU_HP_SLEEP_DIG_CPU_STALL Configures whether to stall HP CPU in HP_SLEEP state.
O: Do not stall
1: Stall
(R/W)
```