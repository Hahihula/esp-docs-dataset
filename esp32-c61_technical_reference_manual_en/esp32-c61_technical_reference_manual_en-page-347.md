

```markdown
## Register 7.12. PCR_LEDC_CONF_REG (0x0034)

PCR_LEDC_CLK_EN Configures whether or not to enable APB_CLK for LEDC.
- O: Not enable
- 1: Enable
(R/W)

PCR_LEDC_RST_EN Configures whether or not to reset LEDC.
- O: Not reset
- 1: Reset
(R/W)

PCR_LEDC_READY Represents whether or not LEDC is released from reset.
- O: Not released
- 1: Released
(RO)
```

```markdown
## Register 7.13. PCR_LEDC_SCLK_CONF_REG (0x0038)

PCR_LEDC_SCL_SEL Configures the clock source of LEDC.
- O (default): XTAL_CLK
- 1: RC_FAST_CLK
- 2: PLL_F80M_CLK
(R/W)

PCR_LEDC_SCLK_EN Configures whether or not to enable FUNC_CLK for LEDC.
- O: Not enable
- 1: Enable
(R/W)
```