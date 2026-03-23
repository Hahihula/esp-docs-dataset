
```markdown
Register 29.10. I2S_RX_TDM_CTRL_REG (0x0050)

| Bit Range | Field Name                          | Description                                                                                                                                                                                                 |
|-----------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31-20     | (reserved)                          |                                                                                                                                                                                                             |
| 19        | I2S_RX_TDM_TOT_CHAN_NUM             | The total number of channels in use in I2S RX TDM mode. Total channel number in use = this value + 1. (R/W)                                                                                                   |
| 18-16     | O                                    |                                                                                                                                                                                                             |
| 15        | OxO                                  |                                                                                                                                                                                                             |
| 14-0      | Reset                                |                                                                                                                                                                                                             |

I2S_RX_TDM_PDM_CHAN_n_EN (n = 0 - 7)   1: Enable the valid data input of I2S RX TDM or PDM channel n. O: Disable. Channel n only inputs O. (R/W)

I2S_RX_TDM_CHAN_n_EN (n = 8 - 15)      1: Enable the valid data input of I2S RX TDM channel n. O: Disable. Channel n only inputs O. (R/W)

Register 29.11. I2S_RXEOF_NUM_REG (0x0064)

| Bit Range | Field Name                          | Description                                                                                                                                                                                                             |
|-----------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31-12     | (reserved)                          |                                                                                                                                                                                                             |
| 11        | Ox40                                 |                                                                                                                                                                                                             |
| 10-0      | Reset                                |                                                                                                                                                                                                             |

I2S_RX_EOF_NUM   The bit length of RX data is (I2S_RX_BITS_MOD + 1) * (I2S_RX_EOF_NUM + 1). Once the length of received data reaches such bit length, an in_sub.eof interrupt is triggered in the configured DMA RX channel. (R/W)
```