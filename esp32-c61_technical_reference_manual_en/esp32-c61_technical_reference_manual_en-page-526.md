

```markdown
Register 11.11. PMU_HP_ACTIVE_HP_REGULATOREG (0x0028)

| Bit | 31 | 27 | 26 | 23 | 22 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 9 | 8 | 4 | 3 | 2 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|
|     |    |    | PMU_HP_ACTIVE_HP_REGULATOR_DBIAS | PMU_HP_ACTIVE_HP_REGULATOR_DBIAS | PMU_HP_ACTIVE_HP_REGULATOR_SLP_MEM_XPD | PMU_HP_ACTIVE_HP_REGULATOR_SLP_LOGIC_XPD | PMU_DIG_REGULATOREG_DBIAS_SEL | (reserved) | PMU_LP_DBIAS_VOL | (reserved) | Reset |
|     | 24 | 12 |    |    |    |    |    |    |    |    |    |    |   |   |   |   |   |   |

PMU_LP_DBIAS_VOL Indicates the voltage level based on PVT_RTC data, which is the feedback from the PVT module in LP_SLEEP state. (RO)

PMU_HP_DBIAS_VOL Indicates the voltage level based on PVT data, which is the feedback from PVT module in HP_SLEEP state. (RO)

PMU_DIG_REGULATOREG_DBIAS_SEL Configures to select the DREG configuration source for main HP and LP regulators in different PMU states.
0: PMU_HP_DBIAS_VOL
1: DREG value of respective main regulators in respective PMU states configured via the following register fields:
  * PMU_HP_ACTIVE_HP_REGULATOR_DBIAS
  * PMU_HP_SLEEP_HP_REGULATOR_DBIAS
  * PMU_HP_ACTIVE_LP_REGULATOR_DBIAS
  * PMU_HP_SLEEP_LP_REGULATOR_DBIAS

(R/W)

PMU_HP_ACTIVE_HP_REGULATOR_SLP_MEM_XPD Configures whether to enable the secondary regulator powering the HP memory in HP_ACTIVE state.
0: Disable
1: Enable
(R/W)

PMU_HP_ACTIVE_HP_REGULATOR_SLP_LOGIC_XPD Configures whether to enable the secondary regulator powering the logic circuit in all HP domains in HP_ACTIVE state.
0: Disable
1: Enable
(R/W)

Continued on the next page...
```