

```markdown
Register 14.1. PMU_HP_ACTIVE_DIG_POWER_REG (0x0000)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| Reset |    |    |    |    |    |    |    |    |    |    |    |    |

PMU_HP_ACTIVE_DCDC_SWITCH_PD_EN Configures whether to cut off the power from external DCDC in HP_ACTIVE state.
O: Do not cut off
1: Cut off
(R/W)

PMU_HP_ACTIVE_HP_MEM_DSLP Configures whether to put L2MEM_GO–G5 into Deep-sleep mode in HP_ACTIVE state.
O: Do not put L2MEM_GO–G5 into Deep-sleep
1: Put L2MEM_GO–G5 into Deep-sleep
(R/W)

PMU_HP_ACTIVE_PD_HP_MEM_PD_EN Configures whether to power down L2MEM_GO–G5 in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)

PMU_HP_ACTIVE_PD_HP_CPU_PD_EN Configures whether to power down the HP_CPU power domain in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)

PMU_HP_ACTIVE_PD_CNNT_PD_EN Configures whether to power down HP_CNNT in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)

PMU_HP_ACTIVE_PD_TOP_PD_EN Configures whether to power down PD_TOP power domain in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)
```