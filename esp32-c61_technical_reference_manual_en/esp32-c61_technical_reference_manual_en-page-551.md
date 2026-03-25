
```markdown
Register 11.40. PMU_HP_SLEEP_LP_REGULATORO_REG (0x009C)

| Bit Range | Field Name                                                                 | Description                                                                                                                                 |
|-----------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 31        | PMU_HP_SLEEP_LP_REGULATOR_DBIAS                                            | Configures the DREG value of the main LP regulator in HP_SLEEP state, adjusting its output voltage. (R/W)                                 |
| 27-24     | PMU_HP_SLEEP_LP_REGULATOR_SLP_XPD                                         | Configures whether to enable the secondary LP regulator in HP_SLEEP state.<br>0: Disable<br>1: Enable (R/W)                              |
| 23        | PMU_HP_SLEEP_LP_REGULATOR_XPD                                              | Configures whether to enable the main LP regulator in HP_SLEEP state.<br>0: Disable<br>1: Enable (R/W)                                   |
| 22-20     | PMU_HP_SLEEP_LP_REGULATOR_SLP_DBIAS                                       | Configures the DREG value of the secondary LP regulator in HP_SLEEP state, adjusting its output voltage. (R/W)                           |
| 19-0      | (reserved)                                                                |                                                                                                                                           |
| Reset     | 0                                                                          |                                                                                                                                           |

PMU_HP_SLEEP_LP_REGULATOR_SLP_XPD Configures whether to enable the secondary LP regulator in HP_SLEEP state.
0: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_LP_REGULATOR_XPD Configures whether to enable the main LP regulator in HP_SLEEP state.
0: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_LP_REGULATOR_SLP_DBIAS Configures the DREG value of the secondary LP regulator in HP_SLEEP state, adjusting its output voltage. (R/W)

PMU_HP_SLEEP_LP_REGULATOR_DBIAS Configures the DREG value of the main LP regulator in HP_SLEEP state, adjusting its output voltage. (R/W)
```