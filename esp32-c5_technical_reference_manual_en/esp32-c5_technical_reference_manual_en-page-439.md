

```markdown
Chapter 9 Reset and Clock

Register 9.58. PCR_IOMUX_CLK_CONF_REG (0x00F4)

31                                 23 22 21 20 19
+------------------------------------------------------------------------------+
| RESERVED | PCR_IOMUX_FUNC_CLK_EN | PCR_IOMUX_FUNC_CLK_SEL |
+------------------------------------------------------------------------------+

PCR_IOMUX_FUNC_CLK_SEL Configures the clock source of IO MUX.
0: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F48M_CLK
3: No clock source
(R/W)

PCR_IOMUX_FUNC_CLK_EN Configures whether or not to enable IO MUX functional clock.
0: Not enable
1: Enable
(R/W)

Register 9.59. PCR_TRACE_CONF_REG (0x00FC)

31                                 2 1 0
+------------------------------------------------------------------------------+
| RESERVED | POR_TRACE_RST_EN | POR_TRACE_CLK_EN |
+------------------------------------------------------------------------------+

PCR_TRACE_CLK_EN Configures whether or not to enable the clock of RISC-V Trace Encoder.
0: Not enable
1: Enable
(R/W)

PCR_TRACE_RST_EN Configures whether or not to reset RISC-V Trace Encoder.
0: Not reset
1: Reset
(R/W)
```