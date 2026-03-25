

```markdown
## Register 13.33. PMU_HP_SLEEP_LP_CK_POWER_REG (0x00AC)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 30  | PMU_HP_SLEEP_XPD_FOSC_CLK    |
| 29  | (reserved)                   |
| 28  | PMU_HP_SLEEP_XPD_XTAL32K     |
| 27  |                              |
| ... | ...                          |
| 0   | Reset                        |

**PMU_HP_SLEEP_XPD_XTAL32K** Configures whether to power up XTAL32K_CLK analog part circuit in HP_ACTIVE/HP_MODEM/HP_SLEEP state.
- O: Power down
- 1: Power up
(R/W)

**PMU_HP_SLEEP_XPD_FOSC_CLK** Configures whether to power up RC_FAST_CLK analog part circuit in HP_ACTIVE/HP_MODEM/HP_SLEEP state.
- O: Power down
- 1: Power up
(R/W)


## Register 13.34. PMU_LP_SLEEP_LP_REGULATORO_REG (0x00B4)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 30  | (reserved)                   |
| 29  | (reserved)                   |
| 28  | PMU_LP_SLEEP_LP_REGULATOR_XPD|
| 27  |                              |
| ... | ...                          |
| 0   | Reset                        |

**PMU_LP_SLEEP_LP_REGULATOR_XPD** Configures whether to enable the LP sys regulator in LP_SLEEP state.
- O: Disable the LP sys regulator
- 1: Enable the LP sys regulator
(R/W)
```