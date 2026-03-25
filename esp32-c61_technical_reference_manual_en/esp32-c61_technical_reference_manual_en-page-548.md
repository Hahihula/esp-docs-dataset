

```markdown
Register 11.36. PMU_HP_SLEEP_SYSCLK_REG (0x008C)

PMU_HP_SLEEP_DIG_SYS_CLK_NO_DIV Configures whether to enable the clock division for HP_ROOT_CLK in HP_SLEEP state. (R/W)

PMU_HP_SLEEP_ICG_SYS_CLOCK_EN Configures whether to enable HP_ROOT_CLK in HP_SLEEP state.
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

PMU_HP_SLEEP_DIG_SYS_CLK_SEL Configures the source of HP_ROOT_CLK in HP_SLEEP state.
O: XTAL
1: PLL_CLK
2: RC_FAST_CLK
3: Invalid value
(R/W)
```