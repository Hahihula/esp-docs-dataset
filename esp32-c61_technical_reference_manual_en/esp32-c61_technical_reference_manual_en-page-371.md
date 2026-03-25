

```markdown
Register 7.48. PCR_TIMEOUT_CONF_REG (0x00E4)

PCR_CPU_TIMEOUT_RST_EN Configures whether or not to reset CPU Peripheral Timeout Protection.
O: Not reset
1: Reset
(R/W)

PCR_HP_TIMEOUT_RST_EN Configures whether or not to reset HP Peripheral Timeout Protection.
O: Not reset
1: Reset
(R/W)
```

```markdown
Register 7.49. PCR_SYSCLK_CONF_REG (0x00E8)

PCR_SOC_CLK_SEL Configures to select the clock source of HP_ROOT_CLK.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F160M_CLK
(R/W)

PCR_CLK_XTAL_FREQ This field indicates the frequency (MHz) of XTAL_CLK. (RO)
```