

```markdown
Register 33.3. RMT_CHnCONFO_REG (n = 0, 1) (0x0010, 0x0014)

Continued from the previous page...

RMT_DIV_CNT_CHn   This field is used to configure the divider for clock of channel n. (R/W)

RMT_MEM_SIZE_CHn  This register is used to configure the maximum number of memory blocks allocated to channel n. (R/W)

RMT_CARRIER_EFF_EN_CHn 1: Add carrier modulation on the output signal only at data-sending state for channel n. 0: Add carrier modulation on the output signal at data-sending state and idle state for channel n. Only valid when RMT_CARRIER_EN_CHn is 1. (R/W)

RMT_CARRIER_EN_CHn This is the carrier modulation enable-bit for channel n. 1: Add carrier modulation on the output signal. 0: No carrier modulation is added on output signal. (R/W)

RMT_CARRIER_OUT_LV_CHn This bit is used to configure the position of carrier wave for channel n. (R/W)

    1’h0: add carrier wave on low level.

    1’h1: add carrier wave on high level.

RMT_CONF_UPDATE_CHn Synchronization bit for channel n (WT)
```