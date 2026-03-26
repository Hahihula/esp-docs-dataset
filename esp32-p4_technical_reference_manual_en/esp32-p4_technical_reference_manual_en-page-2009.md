

```markdown
Register 39.186. H264_DMA_OUT_STATE_CH1_REG (0x0124)

| Bit | Field Name                                 |
|-----|--------------------------------------------|
| 31  | (reserved)                                |
| 25  |                                            |
| 24  |                                            |
| 23  |                                            |
| 20  | H264_DMA_OUT_RESET_AVAIL_CH1              |
| 19  | H264_DMA_OUT_STATE_CH1                    |
| 18  | H264_DMA_OUT_DSCR_STATE_CH1               |
| 17  | H264_DMA_OUTLINK_DSCR_ADDR_CH1            |
| 0   | Reset                                      |

H264_DMA_OUTLINK_DSCR_ADDR_CH1 Represents the current outlink descriptor's address for TX channel 1. (RO)

H264_DMA_OUT_DSCR_STATE_CH1 Represents the current state of the descriptor state machine for TX channel 1. (RO)

H264_DMA_OUT_STATE_CH1 Represents the current control module state machine state for TX channel 1. (RO)

H264_DMA_OUT_RESET_AVAIL_CH1 Represents whether it is safe to reset the channel.
0: Unsafe
1: Safe
(RO)

Register 39.187. H264_DMA_OUT_EOF_DES_ADDR_CH1_REG (0x0128)

| Bit | Field Name                                 |
|-----|--------------------------------------------|
| 31  |                                            |
| 0   | Reset                                      |

H264_DMA_OUT_EOF_DES_ADDR_CH1 Represents the address of the outlink descriptor when the EOF bit in this descriptor is 1. (RO)
```