

```markdown
Register 57.3. RMT_CHnCONFO_REG (n: 0-3) (0x0020+0x4*n)

Continued from the previous page...

RMT_IDLE_OUT_EN_CHn    Configures whether to enable the output for channel n in idle state.
    0: No effect
    1: Enable
    (R/W)

RMT_TX_STOP_CHn        Configures whether to stop the transmitter of channel n sending data out.
    0: No effect
    1: Stop
    (R/W/SC)

RMT_DIV_CNT_CHn        Configures the divider for clock of channel n.
    Measurement unit: rmt_sclk
    (R/W)

RMT_MEM_SIZE_CHn       Configures the maximum number of memory blocks allocated to channel n.
    (R/W)

RMT_CARRIER_EFF_EN_CHn Configures whether to add carrier modulation on the output signal only at data-sending state for channel n.
    0: Add carrier modulation on the output signal at data-sending state and idle state for channel n
    1: Add carrier modulation on the output signal only at data-sending state for channel n
    Only valid when RMT_CARRIER_EN_CHn is 1.
    (R/W)

RMT_CARRIER_EN_CHn     Configures whether to enable the carrier modulation on output signal for channel n.
    0: Disable
    1: Enable
    (R/W)

RMT_CARRIER_OUT_LV_CHn Configures the position of carrier wave for channel n.
    0: Add carrier wave on low level
    1: Add carrier wave on high level
    (R/W)

RMT_CONF_UPDATE_CHn    Synchronization bit for channel n. (WT)

RMT_DMA_ACCESS_EN_CH3   Configures whether to enable the DMA access function for channel 3. This field is reserved for channel 0 ~ 2.
    0: Disable
    1: Enable
    (R/W)
```