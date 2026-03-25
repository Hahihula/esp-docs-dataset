

```markdown
Register 37.2. RMT_CHnCONFO_REG (n: 0-1) (0x0010+0x4*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 1  | 0  | O  | 0x1| RMT_MEM_SIZE_CHn | (reserved) | RMT_CARRIER_EFF_EN_CHn | RMT_CARRIER_OUT_LV_CHn | RMT_UPDATE_CHn | (reserved) | RMT_CONF updating bits |
|     |    |    |    |    |    |    |    |    |    |    |    |    | Reset |

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