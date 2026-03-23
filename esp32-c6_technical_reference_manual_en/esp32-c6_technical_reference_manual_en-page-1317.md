

```markdown
Register 37.3. RMT_CHmCONFO_REG (m: 2-3) (0x0008+0x8*m)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0   | 0  | 1  | 1  | 0  | 0  | 0x1|      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |
|     |    |    |    |    |    |    | RMT_IDLE_THRES_CHm | RMT_CARRIER_OUT_LV_CHm | RMT_CARRIER_EN_CHm | RMT_MEM_SIZE_CHm | (reserved) | (reserved) | RMT_DIV_CNT_CHm | Reset |
```

RMT_DIV_CNT_CHm Configures the clock divider of channel m.
Measurement unit: rmt_sclk
(R/W)

RMT_IDLE_THRES_CHm Configures RX threshold.
When no edge is detected on the input signal for continuous clock cycles longer than this field value, the receiver stops receiving data.
Measurement unit: clk_div
(R/W)

RMT_MEM_SIZE_CHm Configures the maximum number of memory blocks allocated to channel m.
(R/W)

RMT_CARRIER_EN_CHm Configures whether to enable carrier modulation on output signal for channel m.
0: Disable
1: Enable
(R/W)

RMT_CARRIER_OUT_LV_CHm Configures the position of carrier wave for channel m.
0: Add carrier wave on low level
1: Add carrier wave on high level
(R/W)
```