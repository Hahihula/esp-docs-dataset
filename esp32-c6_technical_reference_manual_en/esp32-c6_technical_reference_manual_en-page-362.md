

```markdown
Register 8.68. PCR_PLL_DIV_CLK_EN_REG (0x0128)

Continued from the previous page...

PCR_PLL_40M_CLK_EN    Configures whether or not to enable 40 MHz clock derived from SPPLL divided by 12.
O: Not enable
1 (default): Enable
Only available when high-speed clock source SPPLL is active.
(R/W)

PCR_PLL_20M_CLK_EN    Configures whether or not to enable 20 MHz clock derived from SPPLL divided by 24.
O: Not enable
1 (default): Enable
Only available when high-speed clock source SPPLL is active.
(R/W)


Register 8.69. PCR_CTRL_TICK_CONF_REG (0x0130)

PCR_FOSC_TICK_NUM    Configures the clock divisor for RC_FAST_CLK before it enters the calibration module. (R/W)


Register 8.70. PCR_CTRL_32K_CONF_REG (0x0134)

PCR_32K_SEL   Configures to select one 32 kHz clock for MODEM_SYSTEM and TIMER_GROUP.
O: Invalid
1: Select XTAL32K_CLK
2/3: Select OSC_SLOW_CLK from GPIO0
(R/W)
```