

```markdown
Register 10.22. HP_SYS_CLKRST_PERI_CLK_CTRL15_REG (0x0054)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 30  | HP_SYS_CLKRST_I2S1_TX_CLK_SRC_SEL | Configures the coefficient x for I2S1_RX_CLK clock divisor.                |
| 29  | HP_SYS_CLKRST_I2S1_RX_DIV_YN1   | Configures whether to enable PI2S1_TX_CLK.                                 |
| 28  | HP_SYS_CLKRST_I2S1_RX_DIV_X     | Configures the coefficient x for I2S1_RX_CLK clock divisor. (R/W)           |
| 27  | HP_SYS_CLKRST_I2S1_RX_DIV_Y     | Configures the coefficient y for I2S1_RX_CLK clock divisor. (R/W)           |
| 26  | HP_SYS_CLKRST_I2S1_RX_DIV_Z     | Configures the coefficient z for I2S1_RX_CLK clock divisor. (R/W)           |
| 25  | HP_SYS_CLKRST_I2S1_RX_DIV_YN1   | Configures the coefficient yn1 for I2S1_RX_CLK clock divisor.               |
| 24  | HP_SYS_CLKRST_I2S1_TX_CLK_EN    | 0: Disable<br>1: Enable (R/W)                                              |
| 23  | HP_SYS_CLKRST_I2S1_TX_CLK_SRC_SEL | Configures the clock source for I2S1_TX_CLK.<br>0: XTAL_CLK<br>1: APLL_CLK<br>2: PAD_I2S1_MCLK<br>3: Invalid (R/W) |
```