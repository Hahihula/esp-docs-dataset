

```markdown
Chapter 15 Permission Control (PMS)                                                                 GoBack


Register 15.24. HP_APM_DATE_REG (0x07FC)

HP_APM_DATE Version control register. (R/W)


15.8.2 APM Registers of LP System (LP_APM_REG)


Register 15.25. LP_APM_REGION_FILTER_EN_REG (0x0000)

LP_APM_REGION_FILTER_EN Configure bit n (0-3) to enable region n (0-3).
O: Disable
1: Enable
(R/W)

Register 15.26. LP_APM_REGIONn_ADDR_START_REG (n: 0-3) (0x0004+0xC*n)
LP_APM_REGIONn_ADDR_START Configures the start address of region n. (R/W)
```