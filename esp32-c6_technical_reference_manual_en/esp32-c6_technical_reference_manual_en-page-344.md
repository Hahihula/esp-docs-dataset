

```markdown
Chapter 8 Reset and Clock

Register 8.39. PCR_PWM_CLK_CONF_REG (0x00A0)

PCR_PWM_DIV_NUM Configures the integral part of the frequency divider factor for PWM function clock.
(R/W)

PCR_PWM_CLKM_SEL Configures to select clock source.
O (default): Not select any clock
1: Select PLL_F16OM_CLK
2: Select XTAL_CLK
3: Select RC_FAST_CLK
(R/W)

PCR_PWM_CLKM_EN Configures whether or not to activate PWM_CLKM.
O: Not activate
1: Activate
(R/W)

Register 8.40. PCR_PARL_IO_CONF_REG (0x00A4)

PCR_PARL_CLK_EN Configures whether or not to enable PARL APB clock.
O: Not enable
1: Enable
(R/W)

PCR_PARL_RST_EN Configures whether or not to reset PARL APB register.
O: Not reset
1: Reset
(R/W)
```