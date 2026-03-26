

```markdown
Register 47.3. LP_I2S_RX_CONF1_REG (0x0028)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | (reserved) | LP_I2S_RX_MSB_SHIFT | LP_I2S_RX_TDM_CHAN_BITS | LP_I2S_RX_TDM_WIDTH | LP_I2S_RX_HALF_SAMPLE_BITS | LP_I2S_RX_BITS_MOD | LP_I2S_RX_BCK_DIV_NUM | Reset |
| Value | 0x0 | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF | 0xF |

LP_I2S_RX_TDM_WS_WIDTH Configures the width of LP_I2SI_WS_out (WS default level) at idle level in TDM mode. Width of LP_I2SI_WS_out at idle level in TDM mode = (LP_I2S_RX_TDM_WS_WIDTH[6:0] + 1) x T_BCK. (R/W)

LP_I2S_RX_BCK_DIV_NUM Configures the divider of BCK in RX mode. Note this divider must not be configured to 1. (R/W)

LP_I2S_RX_BITS_MOD Configures the valid data bit length of LP I2S RX channel. Since the LP I2S only supports 16-bit mode, this field must be configured to 15. LP I2S cannot function properly if this field is configured to any other value. (R/W)

LP_I2S_RX_HALF_SAMPLE_BITS Configures LP I2S RX sample bits. BCK cycles in one WS period = I2S_RX_HALF_SAMPLE_BITS x 2. (R/W)

LP_I2S_RX_TDM_CHAN_BITS Configures RX bit number for each channel in TDM mode. Bit number expected = LP_I2S_RX_TDM_CHAN_BITS + 1. (R/W)

LP_I2S_RX_MSB_SHIFT Configures the timing between the WS signal and the MSB of data.
0: Align at the rising edge
1: The WS signal changes one BCK clock earlier
(R/W)
```