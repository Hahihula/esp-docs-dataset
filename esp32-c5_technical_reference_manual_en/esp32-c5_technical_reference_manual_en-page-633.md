

```markdown
Register 13.18. PMU_HP_MODEM_SYSCLK_REG (0x0058)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 0 |
|-----|----|----|----|----|----|----|-----|---|
|     | PMU_HP_MODEM_DIG_SYS_CLK_SEL<br>PMU_HP_MODEM_ICG_SLP_SEL<br>PMU_HP_MODEM_ICG_SYS_CLOCK_EN | (reserved) | Reset |

PMU_HP_MODEM_ICG_SYS_CLOCK_EN Configures whether to enable HP_ROOT_CLK in HP_MODEM state.
O: Disable
1: Enable
(R/W)

PMU_HP_MODEM_SYS_CLK_SLP_SEL Configures whether to allow PMU to control the clock source in HP_MODEM state.
O: Controlled by PCR registers
1: Controlled by PMU
(R/W)

PMU_HP_MODEM_ICG_SLP_SEL Configures whether to allow PMU to control the clock gating in HP_MODEM state.
O: Controlled by PCR registers
1: Controlled by PMU
(R/W)

PMU_HP_MODEM_DIG_SYS_CLK_SEL Configures the source of HP_ROOT_CLK in HP_MODEM state.
O: XTAL
1: PLL_CLK
2: RC_FAST_CLK
3: Invalid value
(R/W)
```