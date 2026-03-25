

```markdown
Register 7.67. PCR_PLL_DIV_CLK_EN_REG (0x0124)

PCR_PLL_96M_CLK_EN Configures whether or not to enable PLL_F96M_CLK.
O: Not enable
1 (default): Enable
(R/W)

PCR_PLL_64M_CLK_EN Configures whether or not to enable PLL_F64M_CLK.
O: Not enable
1 (default): Enable
(R/W)

PCR_PLL_48M_CLK_EN Configures whether or not to enable 48 MHz clock derived from
PLL_F96M_CLK divided by 2.
O: Not enable
1 (default): Enable
(R/W)
```

```markdown
Register 7.68. PCR_CTRL_TICK_CONF_REG (0x012C)

PCR_FOSC_TICK_NUM Configures the clock divisor for RC_FAST_CLK before it enters the calibration module. (R/W)
```