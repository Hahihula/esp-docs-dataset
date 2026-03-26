

```markdown
Register 10.26. HP_SYS_CLKRST_PERI_CLK_CTRL19_REG (0x0064)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
| 30  |                                             |                                                                             |
| 29  |                                             |                                                                             |
| 28  |                                             |                                                                             |
| 27  |                                             |                                                                             |
| 26  |                                             |                                                                             |
|     | HP_SYS_CLKRST_I2S2_TX_DIV_X                | Configures the coefficient x of I2S2_TX_CLK clock divisor. (R/W)            |
|     | HP_SYS_CLKRST_I2S2_TX_DIV_Y                | Configures the coefficient y of I2S2_TX_CLK clock divisor. (R/W)            |
|     | HP_SYS_CLKRST_I2S2_TX_DIV_Z                | Configures the coefficient z of I2S2_TX_CLK clock divisor. (R/W)            |
|     | HP_SYS_CLKRST_I2S2_TX_DIV_YN1              | Configures the coefficient yn1 of I2S2_TX_CLK clock divisor. (R/W)          |
|     | HP_SYS_CLKRST_I2S2_MST_CLK_SEL             | Configures the clock source for output clock PAD_I2S2_MST_CLK.<br>0: I2S2_RX_CLK<br>1: I2S2_TX_CLK (R/W) |
|     | HP_SYS_CLKRST_LCD_CLK_SRC_SEL              | Configures the clock source for LCD_CLK.<br>0: XTAL_CLK<br>1: PLL_F160M_CLK<br>2: APPLL_CLK<br>3: Invalid (R/W) |
|     | HP_SYS_CLKRST_LCD_CLK_EN                   | Configures whether to enable LCD_CLK.<br>0: Disable<br>1: Enable (R/W)       |

Reset
```
```plaintext
HP_SYS_CLKRST_I2S2_TX_DIV_X   Configures the coefficient x of I2S2_TX_CLK clock divisor. (R/W)
HP_SYS_CLKRST_I2S2_TX_DIV_Y   Configures the coefficient y of I2S2_TX_CLK clock divisor. (R/W)
HP_SYS_CLKRST_I2S2_TX_DIV_Z   Configures the coefficient z of I2S2_TX_CLK clock divisor. (R/W)
HP_SYS_CLKRST_I2S2_TX_DIV_YN1 Configures the coefficient yn1 of I2S2_TX_CLK clock divisor. (R/W)
HP_SYS_CLKRST_I2S2_MST_CLK_SEL Configures the clock source for output clock PAD_I2S2_MST_CLK.
    0: I2S2_RX_CLK
    1: I2S2_TX_CLK
    (R/W)
HP_SYS_CLKRST_LCD_CLK_SRC_SEL Configures the clock source for LCD_CLK.
    0: XTAL_CLK
    1: PLL_F160M_CLK
    2: APPLL_CLK
    3: Invalid
    (R/W)
HP_SYS_CLKRST_LCD_CLK_EN Configures whether to enable LCD_CLK.
    0: Disable
    1: Enable
    (R/W)
```