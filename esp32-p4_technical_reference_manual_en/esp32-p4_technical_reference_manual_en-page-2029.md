
```markdown
Register 39.228. H264_DMA_IN_STATE_CHO_REG (0x0524)

H264_DMA_INLINK_DSCR_ADDR_CHO   Represents the current inlink descriptor’s address for RX channel 0. (RO)

H264_DMA_IN_DSCR_STATE_CHO      Represents the current state of the descriptor state machine for RX channel 0. (RO)

H264_DMA_IN_STATE_CHO           Represents the current control module state machine state for RX channel 0. (RO)

H264_DMA_IN_RESET_AVAIL_CHO     Represents whether it is safe to reset the channel.
    0: Unsafe
    1: Safe
    (RO)

Register 39.229. H264_DMA_IN_SUC_EOF_DES_ADDR_CHO_REG (0x0528)

H264_DMA_IN_SUC_EOF_DES_ADDR_CHO Represents the address of the inlink descriptor when the EOF bit in this descriptor is 1. (RO)
```