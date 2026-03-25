

```markdown
Register 9.18. PCR_LEDC_SCLK_CONF_REG (0x004C)

PCR_LEDC_SCLK_SEL Configures the clock source of LEDC.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: No clock source
(R/W)

PCR_LEDC_SCLK_EN Configures whether or not to enable LEDC functional clock.
O: Not enable
1: Enable
(R/W)

Register 9.19. PCR_LEDC_PD_CTRL_REG (0x0050)

PCR_LEDC_MEM_FORCE_PU Configures whether or not to force power up LEDC memory.
O: Not force power up
1: Force power up
(R/W)

PCR_LEDC_MEM_FORCE_PD Configures whether or not to force power down LEDC memory.
O: Not force power down
1: Force power down
(R/W)
```