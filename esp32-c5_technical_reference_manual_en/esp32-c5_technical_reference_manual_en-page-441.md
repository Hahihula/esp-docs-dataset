

```markdown
Register 9.62. PCR_TIMEOUT_CONF_REG (0x010C)

PCR_CPU_TIMEOUT_RST_EN Configures whether or not to reset CPU Peripheral Timeout Protection.
O: Not reset
1: Reset
(R/W)

PCR_HP_TIMEOUT_RST_EN Configures whether or not to reset HP Peripheral Timeout Protection.
O: Not reset
1: Reset
(R/W)


Register 9.63. PCR_SYSCLK_CONF_REG (0x0110)

PCR_SOC_CLK_SEL Configures to select clock source of HP_ROOT_CLK.
O: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F160M_CLK
3: PLL_F240M_CLK □□
(R/W)

PCR_CLK_XTAL_FREQ Represents the frequency of XTAL.
Measurement unit: MHz.
(RO)
```