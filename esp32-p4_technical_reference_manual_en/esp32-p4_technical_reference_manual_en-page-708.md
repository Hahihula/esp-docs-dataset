

```markdown
Register 10.40. HP_SYS_CLKRST_PERI_CLK_CTRL22_REG (0x009C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | O                                                                             |
| 30  | O                                                                             |
| 29  | O                                                                             |
| 28  | HP_SYS_CLKRST_ADC_CLK_SRC_SEL                                               |
| 27  | HP_SYS_CLKRST_RMT_CLK_DIV_DENOMINATOR                                       |
| 26  | HP_SYS_CLKRST_RMT_CLK_DIV_NUMERATOR                                         |
| 25  | HP_SYS_CLKRST_RMT_CLK_DIV_NUM                                              |
| 24  | O                                                                             |
| 23  | O                                                                             |
| 22  | O                                                                             |
| 21  | O                                                                             |
| 20  | O                                                                             |
| 19  | O                                                                             |
| 18  | O                                                                             |
| 17  | HP_SYS_CLKRST_RMT_CLK_SRC_SEL                                              |
| 16  | HP_SYS_CLKRST_LEDC_CLK_SRC_SEL                                             |
| 15  | Reset                                                                         |

HP_SYS_CLKRST_LEDC_CLK_SRC_SEL Configures the clock source for LEDC_CLK.
0: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_LEDC_CLK_EN Configures whether to enable LEDC_CLK.
0: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_RMT_CLK_SRC_SEL Configures the clock source for RMT_CLK.
0: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_RMT_CLK_EN Configures whether to enable RMT_CLK.
0: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_RMT_CLK_DIV_NUM Configures the integer part of the RMT_CLK clock divisor.
(R/W)

HP_SYS_CLKRST_RMT_CLK_DIV_NUMERATOR Configures the numerator of the divisor's fractional part for RMT_CLK. (R/W)

HP_SYS_CLKRST_RMT_CLK_DIV_DENOMINATOR Configures the denominator of the divisor's fractional part for RMT_CLK. (R/W)
```
Continued on the next page...
```