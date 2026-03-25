

```markdown
Register 18.7. LP_ANA_INT_ENA_REG (0x0018)

LP_ANA_BOD_MODEO_INT_ENA

Write 1 to enable LP_ANA_BOD_MODEO_INT. (R/W)


Register 18.8. LP_ANA_INT_CLR_REG (0x001C)

LP_ANA_BOD_MODEO_INT_CLR

Write 1 to clear LP_ANA_BOD_MODEO_INT. (WT)


Register 18.9. LP_ANA_DATE_REG (0x03FC)

LP_ANA_CLK_EN

LP_ANA_LP_ANA_DATE Version control register. (R/W)

LP_ANA_CLK_EN Configures whether to force enable register clock.
0: Automatic clock gating
1: Force enable register clock
The configuration of this field does not affect the register access.
(R/W)
```