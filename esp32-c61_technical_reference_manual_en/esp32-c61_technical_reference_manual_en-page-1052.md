

```markdown
Register 28.9. I2S_RX_TDM_CTRL_REG (0x0050)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31        |                                | (reserved)                                                                  |
| 20..19    |                                 |                                                                             |
| 16..14    | I2S_RX_TDM_TOT_CHAN_NUM         | Configures the total number of channels in use in I2S RX TDM mode. Total channel number in use = I2S_RX_TDM_TOT_CHAN_NUM + 1. (R/W) |
| 15        |                                 |                                                                             |
| 14..8     | I2S_RX_TDM_CHANn_EN (n: 0-7)    | Configures whether to enable the valid data input of I2S RX TDM or PDM channel n.<br>0: Disable. Channel n only inputs 0<br>1: Enable (R/W) |
| 7..6      |                                 |                                                                             |
| 5..3      | I2S_RX_TDM_CHANn_EN (n: 8-15)   | Configures whether to enable the valid data input of I2S RX TDM channel n.<br>0: Disable. Channel n only inputs 0<br>1: Enable (R/W) |
| 2..0      |                                 |                                                                             |

Register 28.10. I2S_RXEOF_NUM_REG (0x0064)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31        |                                | (reserved)                                                                  |
| 12..11    |                                 |                                                                             |
| 0         | I2S_RX_EOF_NUM                 | Configures the bit length of RX data. Bit length of RX data = (I2S_RX_BITS_MOD + 1) x (I2S_RX_EOF_NUM + 1). Once the received data reaches such bit length, a GDMA_IN_SUC_EOF_CHn_INT interrupt is triggered in the configured GDMA RX channel. (R/W) |
```