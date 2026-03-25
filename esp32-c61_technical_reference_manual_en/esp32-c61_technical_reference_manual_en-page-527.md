

```markdown
Chapter 11 Low-Power Management

Register 11.11. PMU_HP_ACTIVE_HP_REGULATOR0_REG (0x0028)

Continued from the previous page...

PMU_HP_ACTIVE_HP_REGULATOR_XPD Configures whether to enable the main HP regulator in HP_ACTIVE state.
O: Disable
1: Enable
(R/W)

PMU_HP_ACTIVE_HP_REGULATOR_SLP_MEM_DBIAS Configures the DREG value of the secondary HP regulator powering the HP memory in HP_ACTIVE state, adjusting its output voltage. (R/W)

PMU_HP_ACTIVE_HP_REGULATOR_SLP_LOGIC_DBIAS Configures the DREG value of the secondary HP regulator powering the logic circuits in HP domain in HP_ACTIVE state, adjusting its output voltage. (R/W)

PMU_HP_ACTIVE_HP_REGULATOR_DBIAS Configures the DREG value of the main HP regulator in HP_ACTIVE state, adjusting its output voltage. (R/W)

Register 11.12. PMU_HP_ACTIVE_HP_REGULATOR1_REG (0x002C)
```

```markdown
| 31 | RESERVED | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----------|---|---|---|---|---|---|---|---|---|
|     | PMU_HP_ACTIVE_HP_REGULATOR_DRV_B | (reserved) | Reset |
| Ox0000 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

PMU_HP_ACTIVE_HP_REGULATOR_DRV_B Configures the drive strength of the main HP regulator in HP_ACTIVE state. (R/W)
```