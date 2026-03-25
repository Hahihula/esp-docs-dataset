

```markdown
Register 28.13. I2S_TX_TDM_CTRL_REG (0x0054)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | O  | 0xO |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |

I2S_TX_TDM_CHANn_EN (n: 0-15) Configures whether to enable the valid data output of I2S TX TDM channel n.
O: Channel TX data is controlled by I2S_TX_CHAN_EQUAL and I2S_SINGLE_DATA. See Section 28.9.2.1
1: Enable
(R/W)

I2S_TX_TDM_TOT_CHAN_NUM Configures the total number of channels in use in I2S TX TDM mode.
Total channel number in use = I2S_TX_TDM_TOT_CHAN_NUM + 1. (R/W)

I2S_TX_TDM_SKIP_MSK_EN Configures the data to be sent in GDMA TX buffer.
O: Data stored in GDMA TX buffer is used by enabled channels and will not be read by channels that are not enabled.
1: Data stored in GDMA TX buffer is read by all channels and will be skipped by channels that are not enabled.
(R/W)
```