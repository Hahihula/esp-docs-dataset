

```markdown
Chapter 9 Reset and Clock

Register 9.86. LP_CLKRST_LP_CLK_CONF_REG (0x0000)

LP_CLKRST_SLOW_CLK_SEL Configures the source of LP_SLOW_CLK.
0: RC_SLOW_CLK
1: XTAL32K_CLK
2: OSC_SLOW_CLK
3: Invalid. No effect

(R/W)

LP_CLKRST_FAST_CLK_SEL Configures the source of LP_FAST_CLK.
0: RC_FAST_CLK
1: XTAL_D2_CLK

(R/W)
```