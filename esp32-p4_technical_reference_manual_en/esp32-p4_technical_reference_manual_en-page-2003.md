

```markdown
Register 39.175. H264_DMA_OUT_STATE_CHO_REG (0x0024)

H264_DMA_OUTLINK_DSCR_ADDR_CHO   Represents the current outlink descriptor's address for TX channel 0. (RO)

H264_DMA_OUT_DSCR_STATE_CHO      Represents the current state of the descriptor state machine for TX channel 0. (RO)

H264_DMA_OUT_STATE_CHO           Represents the current control module state machine state for TX channel 0. (RO)

H264_DMA_OUT_RESET_AVAIL_CHO     Represents whether it is safe to reset the channel.
    0: Unsafe
    1: Safe
    (RO)

Register 39.176. H264_DMA_OUT_EOF_DES_ADDR_CHO_REG (0x0028)

H264_DMA_OUT_EOF_DES_ADDR_CHO     Represents the address of the outlink descriptor when the EOF bit in this descriptor is 1. (RO)
```