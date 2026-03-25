

```markdown
Register 11.43. PMU_HP_SLEEP_LP_CK_POWER_REG (0x00AC)
```

| Bit | 31 | 30 | 29 | 28 | 27 | ... | Reset |
|-----|----|----|----|----|----|-----|-------|
|     | 0  | 1  | 0  | 0  | 0  | 0   | 0     |

```markdown
PMU_HP_SLEEP_XPD_XTAL32K Configures whether to power up XTAL32K_CLK in HP_ACTIVE, HP_MODEM and HP_SLEEP states.
O: Power down
1: Power up
(R/W)

PMU_HP_SLEEP_XPD_RC32K Configures whether to power up RC32K_CLK in HP_ACTIVE, HP_MODEM and HP_SLEEP states.
O: Power down
1: Power up
(R/W)

PMU_HP_SLEEP_XPD_FOSC_CLK Configures whether to power up RC_FAST_CLK in HP_ACTIVE, HP_MODEM and HP_SLEEP states.
O: Power down
1: Power up
(R/W)

PMU_HP_SLEEP_PD_OSC_CLK Configures whether to power up SOSC_CLK in HP_ACTIVE, HP_MODEM and HP_SLEEP states.
O: Power down
1: Power up
(R/W)
```