

```markdown
Chapter 12 Low-Power Management

Register 12.35. PMU_LP_SLEEP_LP_CK_POWER_REG (0x00C4)

| Bit | Description                        |
|-----|------------------------------------|
| 31  | (reserved)                         |
| 30  | PMU_LP_SLEEP_XPD_FOSC_CLK          |
| 29  | (reserved)                         |
| 28  | PMU_LP_SLEEP_XPD_XTAL32K           |
| 27  |                                    |
| ... |                                    |
| 0   | Reset                              |

PMU_LP_SLEEP_XPD_XTAL32K Configures whether to power up XTAL32K_CLK analog part circuit in LP_SLEEP state.
O: Power down
1: Power up
(R/W)

PMU_LP_SLEEP_XPD_FOSC_CLK Configures whether to power up RC_FAST_CLK analog part circuit in LP_SLEEP state.
O: Power down
1: Power up
(R/W)

Register 12.36. PMU_IMM_PAD_HOLD_ALL_REG (0x00E4)

| Bit | Description                        |
|-----|------------------------------------|
| 31  | (reserved)                         |
| 30  | PMU_TIE_LOW_HP_PAD_HOLD_ALL        |
| 29  | PMU_TIE_HIGH_HP_PAD_HOLD_ALL       |
| 28  | PMU_TIE_LOW_LP_PAD_HOLD_ALL        |
| 27  | PMU_TIE_HIGH_LP_PAD_HOLD_ALL       |
| ... |                                    |
| 0   | Reset                              |

PMU_TIE_HIGH_LP_PAD_HOLD_ALL Enables the global Hold signal for the LP pads. (WT)
PMU_TIE_LOW_LP_PAD_HOLD_ALL Disables the global Hold signal for the LP pads. (WT)
PMU_TIE_HIGH_HP_PAD_HOLD_ALL Enables the global Hold signal for the digital pads. (WT)
PMU_TIE_LOW_HP_PAD_HOLD_ALL Disables the global Hold signal for the digital pads. (WT)
```