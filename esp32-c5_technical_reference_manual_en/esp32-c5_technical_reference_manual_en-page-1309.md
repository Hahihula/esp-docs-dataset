

```markdown
Register 35.7. I2S_RX_TDM_CTRL_REG (0x0050)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    | 0  | O  | OxO | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | Reset |

I2S_RX_TDM_PDM_CHAN_EN (n: 0-7) Configures whether to enable the valid data input of I2S RX TDM or PDM channel n.
0: Disable. Channel n only inputs 0
1: Enable
(R/W)

I2S_RX_TDM_CHANn_EN (n: 8-15) Configures whether to enable the valid data input of I2S RX TDM channel n.
0: Disable. Channel n only inputs 0
1: Enable
(R/W)

I2S_RX_TDM_TOT_CHAN_NUM Configures the total number of channels in use in I2S RX TDM mode. Total channel number in use = I2S_RX_TDM_TOT_CHAN_NUM + 1. (R/W)
```

```markdown
Register 35.8. I2S_RXEOF_NUM_REG (0x0064)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    | 0  | O  | Ox40 | Reset |

I2S_RX_EOF_NUM Configures the bit length of RX data. Bit length of RX data = (I2S_RX_BITS_MOD + 1) x (I2S_RX_EOF_NUM + 1). Once the received data reaches such bit length, an AHB_DMA_IN_SUC_EOF_CHn_INT interrupt is triggered in the configured GDMA RX channel.
(R/W)
```