

```markdown
Register 14.33. PMU_POWER_CK_WAIT_CNTL_REG (0x011C)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        | PMU_WAIT_XTL_STABLE                                                         |
|           | Configures the wait time for enabling XTAL global clock gating after the   |
|           | XTAL power supply is enabled. The unit is LP_DYN_FAST_CLK. (R/W)            |
| 16-15     | PMU_WAIT_PLL_STABLE                                                         |
|           | Configures the wait time for enabling PLL global clock gating after the PLL|
|           | power supply is enabled. The unit is LP_DYN_FAST_CLK. (R/W)                 |

Register 14.34. PMU_SLP_WAKEUP_CNTL0_REG (0x0120)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        | PMU_SLEEP_REQ                                                               |
|           | Configures whether to switch the PMU state to HP_SLEEP or LP_SLEEP.         |
|           | 0: Do not switch                                                             |
|           | 1: Switch to HP_SLEEP or LP_SLEEP, depending on the state of the LP CPU. (WT)|

Register 14.35. PMU_SLP_WAKEUP_CNTL1_REG (0x0124)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        | PMU_SLEEP_REJECT_ENA                                                       |
|           | Configures the sleep rejection source. For the mapping between values       |
|           | and sources please refer to Table 14.4-1. (R/W)                              |
|           | PMU_SLP_REJECT_EN                                                            |
|           | Configures whether to enable sleep rejection function.                      |
|           | 0: Disable                                                                  |
|           | 1: Enable                                                                   |
|           | (R/W)                                                                       |
```