

```markdown
Register 12.38. PMU_POWER_CK_WAIT_CNTL_REG (0x011C)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        | PMU_WAIT_PLL_STABLE                                                         |
|           | Configures the number of CLK_DYN_FAST_CLK cycles after which PLL_CLK gate opening is enabled. (R/W) |
| 16-15     | PMU_WAIT_XTAL_STABLE                                                       |
|           | Configures the number of CLK_DYN_FAST_CLK cycles after which XTAL_CLK gate opening is enabled. (R/W) |

Register 12.39. PMU_SLP_WAKEUP_CNTL0_REG (0x0120)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        | PMU_SLEEP_REQ                                                               |
|           | Configures whether to switch the chip’s PMU state to HP_SLEEP or LP_SLEEP.   |
|           | O: Do not switch                                                             |
|           | 1: Switch to HP_SLEEP or LP_SLEEP, depending on the state of the LP CPU. (WT) |

Register 12.40. PMU_SLP_WAKEUP_CNTL1_REG (0x0124)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        | PMU_SLEEP_REJECT_ENA                                                       |
|           | Configures the sleep rejection source. For the mapping between values and sources please refer to Table 12.4-1. (R/W) |
|           | PMU_SLP_REJECT_EN                                                            |
|           | Configures whether to enable sleep rejection function.                       |
|           | O: Disable                                                                  |
|           | 1: Enable                                                                   |
|           | (R/W)                                                                       |
```