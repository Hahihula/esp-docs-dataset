

```markdown
Register 39.250. H264_DMA_IN_STATE_CH2_REG (0x0724)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                                 |                                                                             |
| 24..23    | H264_DMA_IN_RESET_AVAIL_CH2                | Represents whether it is safe to reset the channel. <br> 0: Unsafe <br> 1: Safe (RO) |
| 22..20    | H264_DMA_IN_STATE_CH2                      | Represents the current control module state machine state for RX channel 2. (RO) |
| 19..18    | H264_DMA_IN_DSCR_STATE_CH2                 | Represents the current state of the descriptor state machine for RX channel 2. (RO) |
| 17..0     | H264_DMA_INLINK_DSCR_ADDR_CH2              | Represents the current inlink descriptor’s address for RX channel 2. (RO)      |

Register 39.251. H264_DMA_IN_SUC_EOF_DES_ADDR_CH2_REG (0x0728)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31..0     | (reserved)                                 |                                                                             |
|           |                                         | 0x00000000 Reset                                                             |

H264_DMA_IN_SUC_EOF_DES_ADDR_CH2 Represents the address of the inlink descriptor when the EOF bit in this descriptor is 1. (RO)
```