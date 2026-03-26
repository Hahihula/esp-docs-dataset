

```markdown
Register 39.272. H264_DMA_IN_STATE_CH4_REG (0x0924)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 24  | H264_DMA_IN_RESET_AVAIL_CH4            |                                                                             |
| 23  | H264_DMA_IN_STATE_CH4                  |                                                                             |
| 22  | H264_DMA_IN_DSCR_STATE_ADDR_CH4        | Represents the current inlink descriptor’s address for RX channel 4. (RO)     |
| 21  | H264_DMA_IN_DSCR_STATE_CH4             | Represents the current state of the descriptor state machine for RX channel 4. (RO) |
| 20  | H264_DMA_IN_SUC_EOF_DES_ADDR_CH4       |                                                                             |
| 19  | H264_DMA_IN_RESET_AVAIL_CH4            | Represents whether it is safe to reset the channel.<br>0: Unsafe<br>1: Safe (RO) |
| 18  | H264_DMA_IN_STATE_CH4                  | Represents the current control module state machine state for RX channel 4. (RO) |
| 17  | H264_DMA_IN_DSCR_STATE_ADDR_CH4        |                                                                             |
| 0   | Reset                                  | 0x0000                                                                         |

H264_DMA_INLINK_DSCR_ADDR_CH4 Represents the current inlink descriptor’s address for RX channel 4. (RO)

H264_DMA_IN_DSCR_STATE_ADDR_CH4 Represents the current state of the descriptor state machine for RX channel 4. (RO)

H264_DMA_IN_STATE_CH4 Represents the current control module state machine state for RX channel 4. (RO)

H264_DMA_IN_RESET_AVAIL_CH4 Represents whether it is safe to reset the channel.<br>0: Unsafe<br>1: Safe (RO)

Register 39.273. H264_DMA_IN_SUC_EOF_DES_ADDR_CH4_REG (0x0928)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 0   | Reset                                  | 0x00000000                                                                    |

H264_DMA_IN_SUC_EOF_DES_ADDR_CH4 Represents the address of the inlink descriptor when the EOF bit in this descriptor is 1. (RO)
```