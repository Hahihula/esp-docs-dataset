

```markdown
Register 10.35. HP_SYS_CLKRST_PERI_CLK_CTRL118_REG (0x0088)

| Bit Range | Field Name                                                                 | Description                                                                                                                                 |
|-----------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 31        | (reserved)                                                                | -                                                                                                                                          |
| 27-26     | O                                                                         | Reset                                                                              |
| 19-18     | HP_SYS_CLKRST_PARLIO_RX_CLK_DIV_NUM                                       | Configures the numerator of the divisor's fractional part for clock divider for PARLIO_RX_CLK. (R/W)                                     |
| 17-16     | HP_SYS_CLKRST_PARLIO_TX_CLK_DIV_DENOMINATOR                               | Configures the denominator of the divisor's fractional part for clock divider for PARLIO_RX_CLK. (R/W)                                    |
| 15        | HP_SYS_CLKRST_PARLIO_TX_CLK_SRC_SEL                                     | Configures the clock source for PARLIO_TX_CLK.<br>0: XTAL_CLK<br>1: RC_FAST_CLK<br>2: PLL_F16OM_CLK<br>3: PAD_PARLIO_TX_CLK (R/W) |
| 14        | HP_SYS_CLKRST_PARLIO_TX_CLK_EN                                           | Configures whether to enable PARLIO_TX_CLK.<br>0: Disable<br>1: Enable (R/W)                                                               |
| 13-8      | O                                                                         | Reset                                                                              |
| 7-0       | HP_SYS_CLKRST_PARLIO_TX_CLK_DIV_NUM                                     | Configures the integer part of the clock divisor for PARLIO_TX_CLK. (R/W)                                                                  |

Espressif Systems
```