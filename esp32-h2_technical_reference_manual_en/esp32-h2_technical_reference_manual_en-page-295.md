

```markdown
Register 7.14. PCR_LEDC_CONF_REG (0x003C)

PCR_LEDC_CLK_EN Configures whether or not to enable APB_CLK for LEDC.
O: Not enable
1: Enable
(R/W)

PCR_LEDC_RST_EN Configures whether or not to reset LEDC.
O: Not reset
1: Reset
(R/W)

PCR_LEDC_READY Represents whether or not LEDC is released from reset.
O: Not released
1: Released
(RO)
```

```markdown
Register 7.15. PCR_LEDC_SCLK_CONF_REG (0x0040)

PCR_LEDC_SCLK_SEL Configures the clock source of LEDC.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F96M_CLK
3: No clock source
(R/W)

PCR_LEDC_SCLK_EN Configures whether or not to enable LEDC functional clock.
O: Not enable
1: Enable
(R/W)
```