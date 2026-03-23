

```markdown
Register 12.18. PMU_HP_MODEM_SYSCLK_REG (0x0058)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            |                                                                             |
| 30  | PMU_HP_MODEM_DIG_SYS_CLK_SEL              | Configures the source of HP_ROOT_CLK in HP_MODEM state.                    |
|     |                                            | 0: XTAL<br>1: PLL_CLK<br>2: RC_FAST_CLK<br>3: Invalid value (R/W)           |
| 29  | PMU_HP_MODEM_ICG_SYS_CLOCK_EN             | Configures whether to enable HP_ROOT_CLK in HP_MODEM state.<br>0: Disable<br>1: Enable (R/W) |
| 28  | PMU_HP_MODEM_ICG_SLP_SEL                  | Configures whether to allow PMU to control the clock gating in HP_MODEM state.<br>0: Controlled by PCR registers<br>1: Controlled by PMU (R/W) |
| 27  | PMU_HP_MODEM_SYS_CLK_SLP_SEL              | Configures whether to allow PMU to control the clock source in HP_MODEM state.<br>0: Controlled by PCR registers<br>1: Controlled by PMU (R/W) |
```