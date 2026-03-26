

```markdown
Register 10.36. HP_SYS_CLKRST_PERI_CLK_CTRL119_REG (0x008C)

| Bit | Field Name                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | HP_SYS_CLKRST_CAM_CLK_EN                                                   |
| 29  | HP_SYS_CLKRST_CAM_CLK_SRC_SEL                                              |
| 28  | HP_SYS_CLKRST_I3C_MST_CLK_DIV_NUM                                        |
| 27  | HP_SYS_CLKRST_I3C_MST_CLK_EN                                             |
| 26  | HP_SYS_CLKRST_PARLIO_TX_CLK_DIV_DENOMINATOR                               |
| 19  | HP_SYS_CLKRST_PARLIO_TX_CLK_DIV_NUM                                      |
| 18  | HP_SYS_CLKRST_PARLIO_TX_CLK_DIV_NUM                                      |
| 17  | HP_SYS_CLKRST_CAM_CLK_SRC_SEL                                             |
| 16  | HP_SYS_CLKRST_I3C_MST_CLK_EN                                              |
| 15  | HP_SYS_CLKRST_I3C_MST_CLK_SRC_SEL                                        |
| 8   | Reset                                                                       |

HP_SYS_CLKRST_PARLIO_TX_CLK_DIV_NUMERATOR Configures the numerator of the divisor's fractional part for PARLIO_TX_CLK. (R/W)

HP_SYS_CLKRST_PARLIO_TX_CLK_DIV_DENOMINATOR Configures the denominator of the divisor's fractional part for PARLIO_TX_CLK. (R/W)

HP_SYS_CLKRST_I3C_MST_CLK_SRC_SEL Configures the clock source for I3C_MST_CLK.
0: XTAL_CLK
1: PLL_F160M_CLK
2: PLL_F120M_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_I3C_MST_CLK_EN Configures whether to enable I3C_MST_CLK.
0: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_I3C_MST_CLK_DIV_NUM Configures the integer part of the I3C_MST_CLK clock divisor. (R/W)

HP_SYS_CLKRST_CAM_CLK_SRC_SEL Configures the clock source for the output clock CAM_CLK.
0: XTAL_CLK
1: PLL_F160M_CLK
2: APLL_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_CAM_CLK_EN Configures whether to enable the output clock CAM_CLK.
0: Disable
1: Enable
(R/W)
```