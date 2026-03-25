

```markdown
Register 28.5. I2S_RX_CONF_REG (0x0020)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | I2S_RX_PCK_DIV_NUM                                                          |
| 29  | I2S_RX_PDM_EN                                                                |
| 28  | I2S_RX_TDM_EN                                                                |
| 27  | I2S_RX_BIT_ORDER                                                             |
| 26  | I2S_RX_WS_IDLE_POL                                                           |
| 25  | I2S_RX_FILL_EN                                                               |
| 24  | I2S_RX_LEFT_ALIGN                                                            |
| 23  | (reserved)                                                                  |
| 22  | I2S_RX_MSB_SHIFT                                                              |
| 21  | I2S_RX_PCMypass_CONF                                                         |
| 20  | I2S_RX_MONO_FST_VLD                                                          |
| 19  | I2S_RX_UPDATE                                                                |
| 18  | I2S_RX_BIG_ENDIAN                                                             |
| 17  | I2S_RX_MONO                                                                   |
| 16  | I2S_RX_STOP_MODE                                                              |
| 15  | I2S_RX_SLAVE_MOD                                                              |
| 14  | I2S_RX_START                                                                  |
| 13  | I2S_RX_FIFO_RESET                                                             |
| 12  | (reserved)                                                                   |
| 11  | Oxl                                                                            |
| 10  | 1                                                                             |
| 9   | 0                                                                             |
| 8   | 0                                                                             |
| 7   | 0                                                                             |
| 6   | 0                                                                             |
| 5   | 0                                                                             |
| 4   | 0                                                                             |
| 3   | 0                                                                             |
| 2   | 0                                                                             |
| 1   | 0                                                                             |
| 0   | Reset                                                                         |

I2S_RX_RESET Configures whether to reset RX unit.
O: No effect
1: Reset
(WT)

I2S_RX_FIFO_RESET Configures whether to reset RX FIFO.
O: No effect
1: Reset
(WT)

I2S_RX_START Configures whether to start receiving data.
O: No effect
1: Start
(R/W/SC)

I2S_RX_SLAVE_MOD Configures whether to enable slave RX mode.
O: Enable master mode
1: Enable slave mode
(R/W)

I2S_RX_STOP_MODE Configures when I2S RX stop data reception.
O: Only stops when I2S_RX_START is cleared
1: Stops when I2S_RX_START is cleared or the number of received bytes is greater than the value configured in I2S_RX_EOF_NUM_REG
2: Stops when I2S_RX_START is cleared or GDMA RX FIFO is full
(R/W)

I2S_RX_MONO Configures whether to enable RX unit in mono mode.
O: Disable
1: Enable
(R/W)

I2S_RX_BIG_ENDIAN Configures I2S RX byte endian.
O: Low address data is saved to low address
1: Low address data is saved to high address
(R/W)
```