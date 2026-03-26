

```markdown
Register 10.24. HP_SYS_CLKRST_PERI_CLK_CTRL17_REG (0x005C)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 30  |                                 |                                                                             |
| 29  | HP_SYS_CLKRST_I2S2_RX_DIV_X    | Configures the coefficient x for I2S2_RX_CLK clock divisor.                 |
| 28  |                                 |                                                                             |
| 27  | HP_SYS_CLKRST_I2S2_RX_DIV_N    | Configures the integer part of the clock divisor for I2S2_RX_CLK.           |
| 26  |                                 |                                                                             |
| 25  | HP_SYS_CLKRST_I2S1_TX_DIV_Z    | Configures the coefficient z for I2S1_TX_CLK clock divisor.                 |
| 24  |                                 |                                                                             |
| 23  | HP_SYS_CLKRST_I2S1_TX_DIV_YN1  | Configures the coefficient yn1 for I2S1_TX_CLK clock divisor.               |
| 22  |                                 |                                                                             |
| 21  | HP_SYS_CLKRST_I2S1_MST_CLK_SEL| Configures the clock source for the output clock PAD_I2S1_MST_CLK.          |
|     |                                 | 0: I2S1_RX_CLK                                                               |
|     |                                 | 1: I2S1_TX_CLK                                                               |
|     | (R/W)                          |                                                                             |
| 20  | HP_SYS_CLKRST_I2S2_RX_CLK_EN   | Configures whether to enable I2S2_RX_CLK.                                  |
|     |                                 | 0: Disable                                                                   |
|     |                                 | 1: Enable                                                                     |
|     | (R/W)                          |                                                                             |
| 19  | HP_SYS_CLKRST_I2S2_RX_CLK_SRC_SEL | Configures the clock source for I2S2_RX_CLK.                            |
|     |                                 | 0: XTAL_CLK                                                                   |
|     |                                 | 1: APLL_CLK                                                                   |
|     |                                 | 2: PAD_I2S2_MCLK                                                              |
|     |                                 | 3: Invalid                                                                    |
|     | (R/W)                          |                                                                             |
| 18  | HP_SYS_CLKRST_I2S2_RX_DIV_N    | Configures the integer part of the clock divisor for I2S2_RX_CLK.           |
|     |                                 | (R/W)                                                                         |
| 17  | HP_SYS_CLKRST_I2S2_RX_DIV_X    | Configures the coefficient x for I2S2_RX_CLK clock divisor.                 |
|     |                                 | (R/W)                                                                         |

Espressif Systems
690
ESP32-P4 TRM
PRELIMINARY

Submit Documentation Feedback
```