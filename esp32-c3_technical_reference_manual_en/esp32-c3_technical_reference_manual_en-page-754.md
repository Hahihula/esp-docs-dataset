

```markdown
Register 29.6. I2S_RX_CONF1_REG (0x0028)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | I2S_RX_MSB_SHIFT                                                             |
| 29  | I2S_RX_TDM_CHAN_BITS                                                       |
| 28  | I2S_RX_HALF_SAMPLE_BITS                                                    |
| 27  | I2S_RX_BITS_MOD                                                            |
| 26  | I2S_RX_BCK_DIV_NUM                                                         |
| 25  | I2S_RX_TDM_WS_WIDTH                                                        |

I2S_RX_TDM_WS_WIDTH The width of rx_ws_out (WS default level) in TDM mode is ((I2S_RX_TDM_WS_WIDTH + 1) * T_BCK. (R/W)

I2S_RX_BCK_DIV_NUM Configure the divider of BCK in RX mode. Note this divider must not be configured to 1. (R/W)

I2S_RX_BITS_MOD Configure the valid data bit length of I2S RX channel. 7: all the valid channel data is in 8-bit mode. 15: all the valid channel data is in 16-bit mode. 23: all the valid channel data is in 24-bit mode. 31: all the valid channel data is in 32-bit mode. (R/W)

I2S_RX_HALF_SAMPLE_BITS I2S RX half sample bits. This value x 2 is equal to the BCK cycles in one WS period. (R/W)

I2S_RX_TDM_CHAN_BITS Configure RX bit number for each channel in TDM mode. Bit number expected = this value + 1. (R/W)

I2S_RX_MSB_SHIFT Control the timing between WS signal and the MSB of data. 1: WS signal changes one BCK clock earlier. 0: Align at rising edge. (R/W)
```

```markdown
Register 29.7 I2S_RX_CLKM_CONF_REG (0x0030)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | I2S_MCLK_SEL                                                                |
| 29  | I2S_RX_CLK_SEL                                                              |
| 28  | I2S_RX_CLKM_DIV_NUM                                                         |

I2S_RX_CLKM_DIV_NUM Integral I2S clock divider value. (R/W)

I2S_RX_CLK_ACTIVE Clock enable signal of I2S RX unit. (R/W)

I2S_RX_CLK_SEL Select clock source for I2S RX unit. 0: XTAL_CLK. 1: PLL_D2_CLK. 2: PLL_F160M_CLK. 3: I2S_MCLK_in. (R/W)

I2S_MCLK_SEL 0: Use I2S TX unit clock as I2S_MCLK_OUT. 1: Use I2S RX unit clock as I2S_MCLK_OUT. (R/W)
```