

```markdown
Register 11.69. PMU_POWER_CK_WAIT_CNTL_REG (0x0120)

| Bit Range | Description                     |
|-----------|---------------------------------|
| 31        |                                 |
|           | PMU_WAIT_XTL_STABLE             |
|           |                                 |
| 256       |                                 |
|           |                                 |
| 16        |                                 |
|           | PMU_WAIT_PLL_STABLE             |
|           |                                 |
| 0         |                                 |

PMU_WAIT_XTL_STABLE Configures the number of CLK_DYN_FAST_CLK cycles to delay the XTAL_CLK gate opening after XTAL_CLK powers up, ensuring clock stability during startup. (R/W)

PMU_WAIT_PLL_STABLE Configures the number of CLK_DYN_FAST_CLK cycles to delay the PLL_CLK gate opening after PLL_CLK powers up, ensuring clock stability during startup. (R/W)


Register 11.70. PMU_SLP_WAKEUP_CNTL0_REG (0x0124)

| Bit Range | Description                     |
|-----------|---------------------------------|
| 31        |                                 |
|           | PMU_SLEEP_REQ                   |
|           |                                 |
| 30        | (reserved)                      |
|           |                                 |
| 0         |                                 |

PMU_SLEEP_REQ Configures whether to switch the chip’s PMU state to HP_SLEEP or LP_SLEEP.
0: Do not switch
1: Switch depending on the status of LP CPU.
(WT)
```