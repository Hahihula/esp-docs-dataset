

```markdown
Register 7.22. PCR_SYSTIMER_CONF_REG (0x005C)

PCR_SYSTIMER_CLK_EN    Configures whether or not to enable APB_CLK for System Timer.
O: Not enable
1: Enable
(R/W)

PCR_SYSTIMER_RST_EN    Configures whether or not to reset System Timer.
O: Not reset
1: Reset
(R/W)

PCR_SYSTIMER_READY     Represents whether or not the System Timer is released from reset.
O: Not released
1: Released
(RO)
```

```markdown
Register 7.23. PCR_SYSTIMER_FUNC_CLK_CONF_REG (0x0060)

PCR_SYSTIMER_FUNC_CLK_SEL    Configures the clock source of System Timer.
O (default): XTAL_CLK
1: RC_FAST_CLK
(R/W)

PCR_SYSTIMER_FUNC_CLK_EN     Configures whether or not to enable System Timer functional clock.
O: Not enable
1: Enable
(R/W)
```