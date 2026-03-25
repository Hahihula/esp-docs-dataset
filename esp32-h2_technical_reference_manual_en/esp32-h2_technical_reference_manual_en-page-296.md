

```markdown
Register 7.16. PCR_TIMERGROUP0_CONF_REG (0x0044)

PCR_TGO_CLK_EN Configures whether or not to enable APB_CLK for Timer Group O.
O: Not enable
1: Enable
(R/W)

PCR_TGO_RST_EN Configures whether or not to reset Timer Group O.
O: Not reset
1: Reset
(R/W)

PCR_TGO_WDT_READY Represents whether or not the WDT in Timer Group O is released from reset.
O: Not released
1: Released
(RO)

PCR_TGO_TIMERO_READY Represents whether or not Timer 0 in Timer Group O is released from reset.
O: Not released
1: Released
(RO)

PCR_TGO_TIMER1_READY Represents whether or not Timer 1 in Timer Group O is released from reset.
O: Not released
1: Released
(RO)
```