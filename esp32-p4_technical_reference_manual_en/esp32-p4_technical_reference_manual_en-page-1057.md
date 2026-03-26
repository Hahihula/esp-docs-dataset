

```markdown
Register 14.65. PMU_EXT_LDO_P1_OP2A_ANA_REG (0x01DC)

| 31 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | ... | Reset |
|-----|----:|----:|----:|----:|----:|----:|----:|------|-------|
| 0xb |   0 |   0 | Ox2 |     |     |     |     |      |       |

PMU_ANA_OP2A_MUL_1 Configures the MUL, where the output voltage of the regulator is MUL × Vref.
O-7: MUL ranges from 1 to 2.75, with a step of 0.25.
(R/W)

PMU_ANA_OP2A_EN_VDET_1 Configures whether to enable VO4 voltage detection.
0: Do not enable
1: Enable
(R/W)

PMU_ANA_OP2A_EN_CUR_LIM_1 Configures whether to enable over current protection for VO4.
0: Do not enable
1: Enable
(R/W)

PMU_ANA_OP2A_DREF_1 Configures the LDO Vref, where the output voltage of the regulator is MUL × Vref.
O-8: Vref = 0.5 V - 0.9 V, with a step of 50 mV
9-15: Vref = 1.0 V - 1.6 V, with a step of 100 mV
(R/W)

Register 14.66. PMU_EXT_WAKEUP_LV_REG (0x01E8)

| 31 | Reset |
|----|-------|
|   0 |       |

PMU_EXT_WAKEUP_LV Configures the wake level for EXT wake-up.
0: Low level wake-up
1: High level wake-up
(R/W)
```