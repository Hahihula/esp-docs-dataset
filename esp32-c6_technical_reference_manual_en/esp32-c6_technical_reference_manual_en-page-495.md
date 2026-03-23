

```markdown
Register 12.90. LP_ANA_LP_INT_CLR_REG (0x002C)

LP_ANA_BOD_MODEO_LP_INT_CLR

| 31 | 30 | [31:30] Reserved |
|-----|-----|------------------|
| 0   |     |                  |

LP_ANA_BOD_MODEO_LP_INT_CLR Write 1 to clear LP_ANA_BOD_MODEO_LP_INT. (WT)

Register 12.91. LP_ANA_DATE_REG (0x03FC)

LP_ANA_CLK_EN

| 31 | 30 | [31:30] Version control register. (R/W) |
|-----|-----|------------------------------------------|
| 0   |     |                                          |

LP_ANA_CLK_EN Configures whether to force enable register clock.
O: Automatic clock gating
1: Force enable register clock
The configuration of this field does not effect the access of registers.
(R/W)
```