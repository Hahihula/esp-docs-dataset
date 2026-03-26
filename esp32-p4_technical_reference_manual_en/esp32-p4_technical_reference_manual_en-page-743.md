

```markdown
Chapter 10 Reset and Clock

Register 10.59. LP_CLKRST_LP_CLK_CONF_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 31-12 | (reserved) |
| 11 | 0x0 |
| 10 | 0x0 |
| 9 | 0x0 |
| 8 | LP_CLKRST_ANA_SEL_REF_PLL8M |
| 7 | LP_CLKRST_LP_PERI_DIV_NUM |
| 6 | LP_CLKRST_FAST_CLK_SEL |
| 5 | LP_CLKRST_SLOW_CLK_SEL |

LP_CLKRST_SLOW_CLK_SEL Configures the clock source of LP_SLOW_CLK.
0: RC_SLOW_CLK
1: XTAL32K_CLK
2: Invalid
3: OSC_SLOW_CLK
(R/W)

LP_CLKRST_FAST_CLK_SEL Configures the clock source of LP_FAST_CLK.
0: RC_FAST_CLK
1: XTAL_CLK
2: PLL_LP_CLK
3: Invalid
(R/W)

LP_CLKRST_LP_PERI_DIV_NUM Configures the clock divisor for LP_PERI_CLK. (R/W)

LP_CLKRST_ANA_SEL_REF_PLL8M Configures the reference clock of PLL_LP_CLK.
0: Invalid
1: XTAL32K_CLK
(R/W)
```