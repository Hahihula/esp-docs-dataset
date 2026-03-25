

```markdown
Register 9.15. PCR_RMT_SCLK_CONF_REG (0x0040)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 23  | PCR_RMT_SCLK_EN                                                              |
| 22  | PCR_RMT_SCLK_SEL                                                             |
| 21  | PCR_RMT_SCLK_DIV_NUM                                                        |
| 20  | PCR_RMT_SCLK_DIV_B                                                           |
| 19  | PCR_RMT_SCLK_DIV_A                                                            |
| 12  |                                                                     |
| 11  |                                                                     |
| 6   |                                                                     |
| 5   |                                                                     |
| 0   | Reset                                                                       |

PCR_RMT_SCLK_DIV_A Configures the denominator of the divisor's fractional part for RMT functional clock. (R/W)

PCR_RMT_SCLK_DIV_B Configures the numerator of the divisor's fractional part for RMT functional clock. (R/W)

PCR_RMT_SCLK_DIV_NUM Configures the integral part of the divisor for RMT functional clock. (R/W)

PCR_RMT_SCLK_SEL Configures the clock source of RMT.
0: XTAL_CLK
1 (default): RC_FAST_CLK
2: PLL_F80M_CLK
(R/W)

PCR_RMT_SCLK_EN Configures whether or not to enable RMT functional clock.
0: Not enable
1: Enable
(R/W)
```