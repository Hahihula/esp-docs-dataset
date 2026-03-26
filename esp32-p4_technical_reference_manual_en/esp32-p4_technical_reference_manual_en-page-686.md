

```markdown
Register 10.20. HP_SYS_CLKRST_PERI_CLK_CTRL13_REG (0x004C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  |                                             |                                                                             |
| 29  |                                             |                                                                             |
| 28  | HP_SYS_CLKRST_I2SO_RX_DIV_Z                | Configures the coefficient z of I2SO_RX_CLK clock divisor. (R/W)            |
| 27  |                                             |                                                                             |
| 26  | HP_SYS_CLKRST_I2SO_RX_DIV_YN1              | Configures the coefficient yn1 of I2SO_RX_CLK clock divisor. (R/W)           |
| 25  |                                             |                                                                             |
| 24  | HP_SYS_CLKRST_I2SO_TX_CLK_EN               | Configures whether to enable I2SO_TX_CLK.<br>0: Disable<br>1: Enable (R/W)   |
| 23  |                                             |                                                                             |
| 22  | HP_SYS_CLKRST_I2SO_TX_CLK_SRC_SEL          | Configures the clock source for I2SO_TX_CLK.<br>0: XTAL_CLK<br>1: APLL_CLK<br>2: PAD_I2SO_MCLK<br>3: Invalid (R/W) |
| 21  |                                             |                                                                             |
| 20  | HP_SYS_CLKRST_I2SO_TX_DIV_N                | Configures the integer part of the clock divisor of I2SO_TX_CLK. (R/W)       |
| 19  |                                             |                                                                             |
| 18  | HP_SYS_CLKRST_I2SO_TX_DIV_X                | Configures the coefficient x of I2SO_TX_CLK clock divisor. (R/W)             |
```