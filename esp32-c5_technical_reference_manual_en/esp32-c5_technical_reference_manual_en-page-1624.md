

```markdown
Chapter 42 Remote Control Peripheral (RMT)
Register 42.2. RMT_CHnCONFO_REG (n: 0-1) (0x0010+0x4*n)

Continued from the previous page...

RMT_CARRIER_EN_CHn Configures whether to enable the carrier modulation on output signal for channel n.
O: Disable
1: Enable
(R/W)

RMT_CARRIER_OUT_LV_CHn Configures the position of carrier wave for channel n.
O: Add carrier wave on low level
1: Add carrier wave on high level
(R/W)

RMT_CONF_UPDATE_CHn Synchronization of RMT Channel n. (WT)

Register 42.3. RMT_CHmCONFO_REG (m: 2-3) (0x0018+0x8*(m-2))

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 23 | 22 | ... | 8 | 7 | 0 |
|----|----|----|----|----|----|----|----|----|-----|---|---|---|
| O  | O  | 1  | 0  | 0  |    | 0x1|     |     | Ox7ff|   |   | Reset |
| RMT_DIV_CNT_CHm | Configures the clock divider of channel m.
Measurement unit: rmt_sclk
(R/W)

RMT_IDLE_THRES_CHm Configures RX threshold.
When no edge is detected on the input signal for continuous clock cycles longer than this field value, the receiver stops receiving data.
Measurement unit: clk_div
(R/W)

Continued on the next page...
```