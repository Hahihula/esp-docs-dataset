

```markdown
Chapter 39 H264 Encoder

Register 39.196. H264_DMA_OUT_STATE_CH2_REG (0x0224)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 25  | H264_DMA_OUT_RESET_AVAIL_CH2 |
| 24  | H264_DMA_OUT_STATE_CH2 |
| 23  | H264_DMA_OUT_DSCR_STATE_CH2 |
| 20  | H264_DMA_OUT_LINK_DSCR_ADDR_CH2 |
| 19  | 0x0         |
| 18  | 0x0         |
| 17  |             |
| ... | ...         |
| 0   | Reset       |

H264_DMA_OUTLINK_DSCR_ADDR_CH2 Represents the current outlink descriptor's address for TX channel 2. (RO)

H264_DMA_OUT_DSCR_STATE_CH2 Represents the current state of the descriptor state machine for TX channel 2. (RO)

H264_DMA_OUT_STATE_CH2 Represents the current control module state machine state for TX channel 2. (RO)

H264_DMA_OUT_RESET_AVAIL_CH2 Represents whether it is safe to reset the channel.
0: Unsafe
1: Safe
(RO)

Register 39.197. H264_DMA_OUT_EOF_DES_ADDR_CH2_REG (0x0228)

| Bit | Description |
|-----|-------------|
| 31  |             |
| ... | ...         |
| 0   | Reset       |

H264_DMA_OUT_EOF_DES_ADDR_CH2 Represents the address of the inlink descriptor when the EOF bit in this descriptor is 1. (RO)
```