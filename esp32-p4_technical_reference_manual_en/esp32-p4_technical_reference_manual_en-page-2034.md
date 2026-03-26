

```markdown
Register 39.239. H264_DMA_IN_STATE_CH1_REG (0x0624)

| Bit | Description                              |
|-----|------------------------------------------|
| 31  | (reserved)                               |
| 24  | H264_DMA_IN_DSCR_ADDR_CH1                |
| 23  | H264_DMA_IN_RESET_AVAIL_CH1              |
| 22  | H264_DMA_IN_STATE_CH1                    |
| 20  | H264_DMA_IN_DSCR_STATE_CH1               |
| 19  |                                          |
| 18  |                                          |
| 17  |                                          |
| 1   | 0x0                                      |
| 0   | 0x0                                      |

Reset: 0x000

H264_DMA_INLINK_DSCR_ADDR_CH1 Represents the current inlink descriptor's address for RX channel 1. (RO)

H264_DMA_IN_DSCR_STATE_CH1 Represents the current state of the descriptor state machine for RX channel 1. (RO)

H264_DMA_IN_STATE_CH1 Represents the current control module state machine state for RX channel 1. (RO)

H264_DMA_IN_RESET_AVAIL_CH1 Represents whether it is safe to reset the channel.
0: Unsafe
1: Safe
(RO)

Register 39.240. H264_DMA_IN_SUC_EOF_DES_ADDR_CH1_REG (0x0628)

| Bit | Description                              |
|-----|------------------------------------------|
| 31  |                                          |
|     | 0x0000000                                |

Reset: 0x0000000

H264_DMA_IN_SUC_EOF_DES_ADDR_CH1 Represents the address of the inlink descriptor when the EOF bit in this descriptor is 1. (RO)
```