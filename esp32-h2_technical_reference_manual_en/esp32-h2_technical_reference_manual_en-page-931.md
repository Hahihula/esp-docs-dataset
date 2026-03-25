

```markdown
Register 31.13. I2S_TX_TDM_CTRL_REG (0x0054)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                    |                                                                             |
| 21  | I2S_TX_TDM_SKIP_MSK_EN       | Configures the data to be sent in GDMA TX buffer.                           |
| 20  | I2S_TX_TDM_TOT_CHAN_NUM      | Total channel number in use = I2S_TX_TDM_TOT_CHAN_NUM + 1. (R/W)            |
| 19  | I2S_TX_TDM_CHANNELn_EN        | Configures whether to enable the valid data output of I2S TX TDM channel n.   |
| 16  | O                            | Channel TX data is controlled by I2S_TX_CHAN_EQUAL and I2S_SINGLE_DATA. See Section 31.9.2.1 (R/W) |
| 15  |                                |                                                                             |
| 14  |                                |                                                                             |
| 13  |                                |                                                                             |
| 12  |                                |                                                                             |
| 11  |                                |                                                                             |
| 10  |                                |                                                                             |
| 9   |                                |                                                                             |
| 8   |                                |                                                                             |
| 7   |                                |                                                                             |
| 6   |                                |                                                                             |
| 5   |                                |                                                                             |
| 4   |                                |                                                                             |
| 3   |                                |                                                                             |
| 2   |                                |                                                                             |
| 1   |                                |                                                                             |
| 0   | Reset                        | Ox0                                                                            |

I2S_TX_TDM_CHANNELn_EN (n: 0-15) Configures whether to enable the valid data output of I2S TX TDM channel n.
O: Channel TX data is controlled by I2S_TX_CHAN_EQUAL and I2S_SINGLE_DATA. See Section 31.9.2.1
1: Enable
(R/W)

I2S_TX_TDM_TOT_CHAN_NUM Configures the total number of channels in use in I2S TX TDM mode.
Total channel number in use = I2S_TX_TDM_TOT_CHAN_NUM + 1. (R/W)

I2S_TX_TDM_SKIP_MSK_EN Configures the data to be sent in GDMA TX buffer.
O: Data stored in GDMA TX buffer is used by enabled channels and will not be read by channels that are not enabled.
1: Data stored in GDMA TX buffer is read by all channels and will be skipped by channels that are not enabled.
(R/W)
```