

```markdown
Register 10.21. HP_SYS_CLKRST_PERI_CLK_CTRL14_REG (0x0050)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 30  | O                              | Reset                                                                       |
| 29  | HP_SYS_CLKRST_I2S1_RX_DIV_N    | Configures the integer part of the clock divisor for I2S1_RX_CLK.           |
| 28  | HP_SYS_CLKRST_I2S1_RX_CLK_SRC_SEL | Configures the clock source for I2S1_RX_CLK.<br>0: XTAL_CLK<br>1: APPLL_CLK<br>2: PAD_I2S1_MCLK<br>3: Invalid (R/W) |
| 27  | HP_SYS_CLKRST_I2S1_RX_CLK_EN   | Configures whether to enable I2S1_RX_CLK.<br>0: Disable<br>1: Enable (R/W)     |
| 26  | HP_SYS_CLKRST_I2SO_MST_CLK_SEL | Configures the clock source for the output clock PAD_I2SO_MST_CLK.<br>0: I2SO_RX_CLK<br>1: I2SO_TX_CLK (R/W) |
| 25  | HP_SYS_CLKRST_I2SO_TX_DIV_YN1  | Configures the coefficient yn1 for I2SO_TX_CLK clock divisor.               |
| 24  | HP_SYS_CLKRST_I2SO_TX_DIV_Z    | Configures the coefficient z for I2SO_TX_CLK clock divisor.                 |
| 23  | HP_SYS_CLKRST_I2SO_TX_DIV_Y    | Configures the coefficient y for I2SO_TX_CLK clock divisor.                 |

```