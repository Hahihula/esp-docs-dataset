

```markdown
Register 8.12. PCR_LEDC_CONF_REG (0x0034)

PCR_LEDC_CLK_EN Configures whether or not to enable LEDC APB clock.
O: Not enable
1: Enable
(R/W)

PCR_LEDC_RST_EN Configures whether or not to reset LEDC module.
O: Not reset
1: Reset
(R/W)
```

```markdown
Register 8.13. PCR_LEDC_SCLK_CONF_REG (0x0038)

PCR_LEDC_SCLK_SEL Configures to select clock source.
O (default): Not select any clock
1: Select PLL_F80M_CLK
2: Select RC_FAST_CLK
3: Select XTAL_CLK
(R/W)

PCR_LEDC_SCLK_EN Configures whether or not to enable LEDC function clock.
O: Not enable
1: Enable
(R/W)
```