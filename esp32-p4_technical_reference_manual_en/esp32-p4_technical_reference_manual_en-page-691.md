

```markdown
Register 10.25. HP_SYS_CLKRST_PERI_CLK_CTRL18_REG (0x0060)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  |                                             |                                                                             |
| 29  |                                             |                                                                             |
| 28  | HP_SYS_CLKRST_I2S2_TX_DIV_N                | Configures the integer part for I2S2_TX_CLK clock divisor. (R/W)            |
| 27  |                                             |                                                                             |
| 26  | HP_SYS_CLKRST_I2S2_RX_DIV_Y                | Configures the coefficient y for I2S2_RX_CLK clock divisor. (R/W)           |
| 25  |                                             |                                                                             |
| 24  | HP_SYS_CLKRST_I2S2_RX_DIV_Z                | Configures the coefficient z for I2S2_RX_CLK clock divisor. (R/W)           |
| 23  |                                             |                                                                             |
| 22  | HP_SYS_CLKRST_I2S2_RX_DIV_YN1              | Configures the coefficient yn1 for I2S2_RX_CLK clock divisor. (R/W)         |
| 21  |                                             |                                                                             |
| 20  | HP_SYS_CLKRST_I2S2_TX_CLK_EN               | Configures whether to enable I2S2_TX_CLK.<br>0: Disable<br>1: Enable (R/W)   |
| 19  |                                             |                                                                             |
| 18  | HP_SYS_CLKRST_I2S2_TX_CLK_SRC_SEL          | Configures the clock source for I2S2_TX_CLK.<br>0: XTAL_CLK<br>1: APLL_CLK<br>2: PAD_I2S2_MCLK<br>3: Invalid (R/W) |
| 17  |                                             |                                                                             |
| 16  |                                             |                                                                             |
| 15  |                                             |                                                                             |
| 14  |                                             |                                                                             |
| 13  |                                             |                                                                             |
| 12  |                                             |                                                                             |
| 11  |                                             |                                                                             |
| 10  |                                             |                                                                             |
| 9   | HP_SYS_CLKRST_I2S2_RX_DIV_Z                |                                                                             |
| 8   |                                             |                                                                             |
| 7   |                                             |                                                                             |
| 6   |                                             |                                                                             |
| 5   |                                             |                                                                             |
| 4   |                                             |                                                                             |
| 3   |                                             |                                                                             |
| 2   |                                             |                                                                             |
| 1   |                                             |                                                                             |
| 0   | Reset                                      |                                                                             |

HP_SYS_CLKRST_I2S2_RX_DIV_Y Configures the coefficient y for I2S2_RX_CLK clock divisor. (R/W)

HP_SYS_CLKRST_I2S2_RX_DIV_Z Configures the coefficient z for I2S2_RX_CLK clock divisor. (R/W)

HP_SYS_CLKRST_I2S2_RX_DIV_YN1 Configures the coefficient yn1 for I2S2_RX_CLK clock divisor. (R/W)

HP_SYS_CLKRST_I2S2_TX_CLK_EN Configures whether to enable I2S2_TX_CLK.
0: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_I2S2_TX_CLK_SRC_SEL Configures the clock source for I2S2_TX_CLK.
0: XTAL_CLK
1: APLL_CLK
2: PAD_I2S2_MCLK
3: Invalid
(R/W)

HP_SYS_CLKRST_I2S2_TX_DIV_N Configures the integer part for I2S2_TX_CLK clock divisor. (R/W)
```