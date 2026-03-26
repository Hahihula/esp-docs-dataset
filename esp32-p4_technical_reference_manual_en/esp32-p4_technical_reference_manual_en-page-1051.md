

```markdown
Register 14.59. PMU_EXT_LDO_PO_OP1A_ANA_REG (0x01BC)

| 31 | 28 | 27 | 26 | 25 | 23 | 22 | ... | Reset |
|----:|----:|----:|----:|----:|----:|----:|-----|-------|
| 0xb | 0   | 0x2 |     |     |     |     | (reserved) |       |

PMU_ANA_OP1A_MUL_O Configures the MUL, where the output voltage of the regulator is MUL × Vref.
O-7: MUL ranges from 1 to 2.75, with a step of 0.25.
(R/W)

PMU_ANA_OP1A_EN_VDET_O Configures whether to enable VO1 voltage detection.
0: Do not enable
1: Enable
(R/W)

PMU_ANA_OP1A_EN_CUR_LIM_O Configures whether to enable over current protection for VO1.
0: Do not enable
1: Enable
(R/W)

PMU_ANA_OP1A_DREF_O Configures the LDO Vref, where the output voltage of the regulator is MUL × Vref.
O-8: Vref = 0.5 V - 0.9 V, with a step of 50 mV
9-15: Vref = 1.0 V - 1.6 V, with a step of 100 mV
(R/W)
```