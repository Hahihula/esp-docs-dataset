

```markdown
Chapter 16 Permission Control (PMS) GoBack


Register 16.23. HP_APM_CLOCK_GATE_REG (0x010C)

HP_APM_CLK_EN Configures whether to keep the clock always on.
O: enable automatic clock gating
1: keep the clock always on
(R/W)


Register 16.24. HP_APM_DATE_REG (0x07FC)

HP_APM_DATE Version control register. (R/W)


16.7.2 Low Power APM Registers (LP_APM_REG)

Register 16.25. LP_APM_REGION_FILTER_EN_REG (0x0000)

LP_APM_REGION_FILTER_EN Configure bit n (0-3) to enable region n.
O: disable
1: enable
(R/W)
```