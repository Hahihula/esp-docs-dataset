

```markdown
Register 29.14. I2S_TX_CLKM_CONF_REG (0x0034)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | I2S_CLK_EN                                                                   |
| 29  | I2S_TX_CLK_SEL                                                               |
| 28  | I2S_TX_CLK_ACTIVE                                                            |
| 27  | (reserved)                                                                  |
| 26  | (reserved)                                                                  |
| 25  | (reserved)                                                                  |
| ... | ...                                                                         |
| 0   | Reset                                                                       |

I2S_TX_CLKM_DIV_NUM Integral I2S TX clock divider value. (R/W)
I2S_TX_CLK_ACTIVE I2S TX unit clock enable signal. (R/W)
I2S_TX_CLK_SEL Select clock clock for I2S TX unit. O: XTAL_CLK. 1: PLL_D2_CLK. 2: PLL_F160M_CLK. 3: I2S_MCLK_in. (R/W)
I2S_CLK_EN Set this bit to enable clock gate. (R/W)

Register 29.15. I2S_TX_TDM_CTRL_REG (0x0054)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | O                                                                             |
| ... | ...                                                                         |
| 8   | I2S_TX_TDM_CHAN_EN                                                            |
| 7   | I2S_TX_TDM_SKIP_MSK_EN                                                       |
| 6   | I2S_TX_TDM_TOT_CHAN_NUM                                                     |

I2S_TX_TDM_CHANn_EN (n = 0-15) 1: Enable the valid data output of I2S TX TDM channel n. O: Channel TX data is controlled by I2S_TX_CHAN_EQUAL and I2S_SINGLE_DATA. See Section 29.9.2.1. (R/W)
I2S_TX_TDM_TOT_CHAN_NUM Set the total number of channels in use in I2S TX TDM mode. Total channel number in use = this value + 1. (R/W)
I2S_TX_TDM_SKIP_MSK_EN When DMA TX buffer stores the data of (I2S_TX_TDM_TOT_CHAN_NUM + 1) channels, and only the data of the enabled channels is sent, then this bit should be set. Clear it when all the data stored in DMA TX buffer is for enabled channels. (R/W)
```