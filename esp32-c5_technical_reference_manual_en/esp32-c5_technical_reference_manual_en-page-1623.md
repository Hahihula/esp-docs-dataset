

```markdown
Register 42.2. RMT_CHnCONFO_REG (n: 0-1) (0x0010+0x4*n)

Continued from the previous page...

RMT_TX_CONTI_MODE_CHn Configures whether to enable continuous TX mode for channel n.
O: No Effect
1: Enable
In this mode, the transmitter starts transmission from the first data. If an end-marker is encountered, the transmitter starts transmitting data from the first data again. if no end-marker is encountered, the transmitter starts transmitting the first data again when the last data is transmitted.
(R/W)

RMT_MEM_TX_WRAP_EN_CHn Configures whether to enable wrap TX mode for channel n.
O: No effect
1: Enable
In this mode, if the TX data size is larger than the channel's RAM block size, the transmitter continues transmitting the first data to the last data in loops.
(R/W)

RMT_IDLE_OUT_LV_CHn Configures the level of output signal for channel n when the transmitter is in idle state. (R/W)

RMT_IDLE_OUT_EN_CHn Configures whether to enable the output for channel n in idle state.
O: No effect
1: Enable
(R/W)

RMT_TX_STOP_CHn Configures whether to stop the transmitter of channel n sending data out.
O: No effect
1: Stop
(R/W/SC)

RMT_DIV_CNT_CHn Configures the divider for clock of channel n.
Measurement unit: rmt_sclk
(R/W)

RMT_MEM_SIZE_CHn Configures the maximum number of memory blocks allocated to channel n.
(R/W)

RMT_CARRIER_EFF_EN_CHn Configures whether to add carrier modulation on the output signal only at data-sending state for channel n.
O: Add carrier modulation on the output signal at data-sending state and idle state for channel n
1: Add carrier modulation on the output signal only at data-sending state for channel n
Only valid when RMT_CARRIER_EN_CHn is 1.
(R/W)

Continued on the next page...
```