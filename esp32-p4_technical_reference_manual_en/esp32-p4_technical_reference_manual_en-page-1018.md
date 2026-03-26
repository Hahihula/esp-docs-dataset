

```markdown
Register 14.18. PMU_HP_SLEEP_SYSCLK_REG (0x008C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 0 |
|-----|----|----|----|----|----|----|-----|---|
|     | O  | O  | O  | O  | O  | O  | (reserved) | Reset |

PMU_HP_SLEEP_ICG_SYS_CLOCK_EN Configures whether to enable ROOT_CLK in HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_SYS_CLK_SLP_SEL Configures whether to allow PMU to control the clock source in HP_SLEEP state.
O: Controlled by PCR registers
1: Controlled by PMU
(R/W)

PMU_HP_SLEEP_ICG_SLP_SEL Configures whether to allow PMU to control the clock gating in HP_SLEEP state.
O: Controlled by PCR registers
1: Controlled by PMU
(R/W)

PMU_HP_SLEEP_DIG_SYS_CLK_SEL Configures the source of ROOT_CLK in HP_SLEEP state.
O: XTAL
1: PLL_CLK
2: RC_FAST_CLK
3: Invalid value
(R/W)
```