

```markdown
Register 33.3. RMT_CHnCONFO_REG (n = 0, 1) (0x0010, 0x0014)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 0  |    |    |    |    |    |    | RMT_TX_STOP_CHn | RMT_IDLE_OUT_EN_CHn | RMT_IDLE_OUT_LV_CHn | RMT_CARRIER_EN_CHn | RMT_CARRIER_OUT_LV_CHn | (reserved) | RMT_CARRIER_UPDATE_CHn | (reserved) | RMT_CONF_PEd | (reserved) |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    | RMT_MEM_SIZE_OCHn | RMT_CARRIER_EFF_EN_CHn | RMT_CARRIER_OUT_LV_CHn | (reserved) | RMT_TX_START_CHn | RMT_MEM_RD_RST_CHn | RMT_APB_MEM_RST_CHn | RMT_TX_CONTI_MODE_CHn | RMT_TX_STOP_CHn |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset | 0x1 | Ox2 |

RMT_TX_START_CHn Set this bit to start sending data in channel n. (WT)

RMT_MEM_RD_RST_CHn Set this bit to reset RAM read address accessed by the transmitter for channel n. (WT)

RMT_APB_MEM_RST_CHn Set this bit to reset RAM W/R address accessed by APB FIFO for channel n. (WT)

RMT_TX_CONTI_MODE_CHn Set this bit to enable continuous TX mode for channel n. (R/W)

In this mode, the transmitter starts its transmission from the first data, and in the following transmission:

* if an end-marker is encountered, the transmitter starts transmitting data from the first data again;
* if no end-marker is encountered, the transmitter starts transmitting the first data again when the last data is transmitted.

RMT_MEM_TX_WRAP_EN_CHn Set this bit to enable wrap TX mode for channel n. In this mode, if the TX data size is larger than the channel's RAM block size, the transmitter continues transmitting the first data to the last data in loops. (R/W)

RMT_IDLE_OUT_LV_CHn This bit configures the level of output signal for channel n when the transmitter is in idle state. (R/W)

RMT_IDLE_OUT_EN_CHn This is the output enable-bit for channel n in idle state. (R/W)

RMT_TX_STOP_CHn Set this bit to stop the transmitter of channel n sending data out. (R/W/SC)
```