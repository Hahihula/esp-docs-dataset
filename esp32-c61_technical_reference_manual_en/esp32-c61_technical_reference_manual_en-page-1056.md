

```markdown
Register 28.12. I2S_TX_CONF1_REG (0x002C)

| Bit | Description |
|-----|-------------|
| 31  | I2S_TX_TDM_CHAN_BITS |
| 27  |                 |
| 26  |                 |
| 19  | I2S_TX_HALF_SAMPLE_BITS |
| 18  |                 |
| 14  | I2S_TX_BITS_MOD |
| 13  |                 |
| 9   | (reserved) |
| 8   |                 |
| 0   | I2S_TX_TDM_WS_WIDTH |

Reset: 0x0

I2S_TX_TDM_WS_WIDTH Configures the width of I2SO_WS_out (WS default level) at idle level in TDM mode. The width of I2SO_WS_out at idle level in TDM mode = (I2S_TX_TDM_WS_WIDTH[8:0] + 1) x T_BCK. (R/W)

I2S_TX_BITS_MOD Configures the valid data bit length of I2S TX channel.
7: All the valid channel data is in 8-bit mode
15: All the valid channel data is in 16-bit mode
23: All the valid channel data is in 24-bit mode
31: All the valid channel data is in 32-bit mode
Other values are invalid.
(R/W)

I2S_TX_HALF_SAMPLE_BITS Configures I2S TX sample bits. BCK cycles in one WS period = I2S_TX_HALF_SAMPLE_BITS x 2. (R/W)

I2S_TX_TDM_CHAN_BITS Configures TX bit number for each channel in TDM mode. Bit number expected = I2S_TX_TDM_CHAN_BITS + 1. (R/W)
```