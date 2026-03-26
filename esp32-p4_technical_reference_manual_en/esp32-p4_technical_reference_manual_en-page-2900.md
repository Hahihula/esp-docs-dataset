

```markdown
Register 57.3. RMT_CHnCONFO_REG (n: 0-3) (0x0020+0x4*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | RMT_DMA_ACCESS_EN_CHn                                                       |
| 29  | RMT_CONF_UPDATE_OUT_LV_CHn                                                 |
| 28  | (reserved)                                                                  |
| 27  | RMT_CARRIER_CARRIER_EFF_EN_CHn                                             |
| 26  | RMT_CARRIER_CARRIER_EFF_EN_CHn                                             |
| 25  | RMT_MEM_SIZE_CHn                                                            |
| 24  | RMT_DIV_CNT_CHn                                                             |
| 23  | RMT_TX_STOP_CHn                                                             |
| 22  | RMT_IDLE_OUT_EN_CHn                                                         |
| 21  | RMT_MEM_TX_WRAP_EN_CHn                                                     |
| 20  | RMT_TX_CONTI_MODE_CHn                                                      |
| 19  | RMT_TX_APB_MEM_RST_CHn                                                     |
| 18  | RMT_TX_START_CHn                                                            |
| 17  | (reserved)                                                                  |
| 16  | Ox1                                                                        |
| 15  | Ox2                                                                        |
| 14  | Reset                                                                      |

RMT_TX_START_CHn Configures whether to enable sending data in channel n.
O: No effect
1: Enable
(WT)

RMT_MEM_RD_RST_CHn Configures whether to reset RAM read address accessed by the transmitter for channel n.
O: No effect
1: Reset
(WT)

RMT_APB_MEM_RST_CHn Configures whether to reset RAM W/R address accessed by APB FIFO for channel n.
O: No effect
1: Reset
(WT)

RMT_TX_CONTI_MODE_CHn Configures whether to enable continuous TX mode for channel n.
O: No Effect
1: Enable
In this mode, the transmitter starts transmission from the first data. If an end-marker is encountered, the transmitter starts transmitting data from the first data again; if no end-marker is encountered, the transmitter starts transmitting the first data again when the last data is transmitted.
(R/W)

RMT_MEM_TX_WRAP_EN_CHn Configures whether to enable wrap TX mode for channel n.
O: No effect
1: Enable
In this mode, if the TX data size is larger than the channel's RAM block size, the transmitter continues transmitting the first data to the last data in loops.
(R/W)

RMT_IDLE_OUT_LV_CHn Configures the level of output signal for channel n when the transmitter is in idle state. (R/W)
```
Continued on the next page...
```