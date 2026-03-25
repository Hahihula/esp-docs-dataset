

```markdown
Register 35.5. I2S_RX_CONF_REG (0x0020)

| Bit | Description                     |
|-----|---------------------------------|
| 31  | (reserved)                      |
| 30  | (reserved)                      |
| 29  | (reserved)                      |
| 28  | (reserved)                      |
| 27  | I2S_RX_PDM_EN                   |
| 26  | I2S_RX_TDM_EN                   |
| 25  | I2S_RX_WS_BIT_ORDER            |
| 24  | I2S_RX_IDLE_POL                 |
| 23  | I2S_RX_FILL_EN                  |
| 22  | I2S_RX_LEFT_ALONE               |
| 21  | I2S_RX_MSB_MODE                 |
| 20  | I2S_RX_PCMGF_BYPASS             |
| 19  | I2S_RX_CONF                      |
| 18  | I2S_RX_FST_VLD                  |
| 17  | I2S_RX_UPDATE                   |
| 16  | I2S_RX_BIG_ENDIAN               |
| 15  | I2S_RX_MONO                     |
| 14  | I2S_RX_STOP_MODE                |
| 13  | I2S_RX_SLAVE_MOD                |
| 12  | I2S_RX_START                    |
| 11  | I2S_RX_FIFO_RESET               |
| 10  | (reserved)                      |
| 9   | (reserved)                      |
| 8   | (reserved)                      |
| 7   | (reserved)                      |
| 6   | (reserved)                      |
| 5   | (reserved)                      |
| 4   | (reserved)                      |
| 3   | (reserved)                      |
| 2   | (reserved)                      |
| 1   | (reserved)                      |
| 0   | Reset                           |

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