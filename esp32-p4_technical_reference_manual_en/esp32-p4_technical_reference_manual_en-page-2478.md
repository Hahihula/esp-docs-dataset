

```markdown
Register 46.6. I2S_RX_CONF1_REG (0x0028)

| 31 | 27 | 26 | 19 | 18 | 14 | 13 | 9 | 8 | 0 |
|-----:|:----|:----|:----|:----|:----|:----|:--|:--|:--|
| Oxf | Oxf |     | Oxf |    | 0 | 0 | 0 | 0 | Ox0 |

Reset

I2S_RX_TDM_WS_WIDTH Configures the width of I2SnI_WS_out (WS default level) at idle level in TDM mode. Width of I2SnI_WS_out at idle level in TDM mode = (I2S_RX_TDM_WS_WIDTH[8:0] +1) x T_BCK. (R/W)

I2S_RX_BITS_MOD Configures the valid data bit length of I2S RX channel.
7: All the valid channel data is in 8-bit mode
15: All the valid channel data is in 16-bit mode
23: All the valid channel data is in 24-bit mode
31: All the valid channel data is in 32-bit mode
Other values are invalid.
(R/W)

I2S_RX_HALF_SAMPLE_BITS Configures I2S RX sample bits. BCK cycles in one WS period = I2S_RX_HALF_SAMPLE_BITS x 2. (R/W)

I2S_RX_TDM_CHAN_BITS Configures RX bit number for each channel in TDM mode. Bit number expected = I2S_RX_TDM_CHAN_BITS + 1. (R/W)
```