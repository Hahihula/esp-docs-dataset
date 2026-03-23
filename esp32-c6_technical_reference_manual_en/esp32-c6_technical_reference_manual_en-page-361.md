

```markdown
Chapter 8 Reset and Clock

Register 8.68. PCR_PLL_DIV_CLK_EN_REG (0x0128)

PCR_PLL_240M_CLK_EN Configures whether or not to enable 240 MHz clock derived from SPPLL divided by 2.
O: Not enable
1 (default): Enable
Only available when high-speed clock source SPPLL is active.
(R/W)

PCR_PLL_160M_CLK_EN Configures whether or not to enable 160 MHz clock derived from SPPLL divided by 3.
O: Not enable
1 (default): Enable
Only available when high-speed clock source SPPLL is active.
(R/W)

PCR_PLL_120M_CLK_EN Configures whether or not to enable 120 MHz clock derived from SPPLL divided by 4.
O: Not enable
1 (default): Enable
Only available when high-speed clock source SPPLL is active.
(R/W)

PCR_PLL_80M_CLK_EN Configures whether or not to enable 80 MHz clock derived from SPPLL divided by 6.
O: Not enable
1 (default): Enable
Only available when high-speed clock source SPPLL is active.
(R/W)

PCR_PLL_48M_CLK_EN Configures whether or not to enable 48 MHz clock derived from SPPLL divided by 10.
O: Not enable
1 (default): Enable
Only available when high-speed clock source SPPLL is active.
(R/W)
```