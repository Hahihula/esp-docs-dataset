

```markdown
Register 11.10. PMU_HP_ACTIVE_SYSCLK_REG (0x0024)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | ... | 0 |
|-----|----|----|----|----|----|----|----|-----|---|
|     |    |    |    |    |    |    |    | (reserved) | Reset |

PMU_HP_ACTIVE_DIG_SYS_CLK_SEL
PMU_HP_ACTIVE_ICG_SYS_CLOCK_EN
PMU_HP_ACTIVE_ICG_SYS_SLP_SEL
PMU_HP_ACTIVE_SYS_CLK_NO_DIV

PMU_HP_ACTIVE_DIG_SYS_CLK_NO_DIV Configures whether to enable the clock division for HP_ROOT_CLK in HP_ACTIVE state. (R/W)

PMU_HP_ACTIVE_ICG_SYS_CLOCK_EN Configures whether to enable HP_ROOT_CLK in HP_ACTIVE state.
0: Disable
1: Enable
(R/W)

PMU_HP_ACTIVE_SYS_CLK_SLP_SEL Configures whether to allow PMU to control clock source in HP_ACTIVE state.
0: Controlled by PCR registers
1: Controlled by PMU
(R/W)

PMU_HP_ACTIVE_ICG_SLP_SEL Configures whether to allow PMU to control the clock gating in HP_ACTIVE state.
0: Controlled by PCR registers
1: Controlled by PMU
(R/W)

PMU_HP_ACTIVE_DIG_SYS_CLK_SEL Configures the source of HP_ROOT_CLK in HP_ACTIVE state.
0: XTAL
1: PLL_CLK
2: RC_FAST_CLK
3: Invalid value
(R/W)
```