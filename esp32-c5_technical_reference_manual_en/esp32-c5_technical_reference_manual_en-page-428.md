

```markdown
Register 9.41. PCR_PWM_CLK_CONF_REG (0x00A8)

PCR_PWM_DIV_NUM Configures the integral part of the divisor for MCPWM functional clock. (R/W)

PCR_PWM_CLKM_SEL Configures the clock source of MCPWM.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F16OM_CLK
3: No clock source
(R/W)

PCR_PWM_CLKM_EN Configures whether or not to enable MCPWM functional clock.
O: Not enable
1: Enable
(R/W)
```

```markdown
Register 9.42. PCR_PARL_IO_CONF_REG (0x00AC)

PCR_PARL_CLK_EN Configures whether or not to enable APB_CLK for Parallel IO.
O: Not enable
1: Enable
(R/W)

PCR_PARL_RST_EN Configures whether or not to reset Parallel IO APB registers.
O: Not reset
1: Reset
(R/W)

PCR_PARL_READY Represents whether or not Parallel IO is released from reset.
O: Not released
1: Released
(RO)
```