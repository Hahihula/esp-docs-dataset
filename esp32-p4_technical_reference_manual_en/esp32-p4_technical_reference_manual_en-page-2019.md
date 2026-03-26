

```markdown
Register 39.206. H264_DMA_OUT_STATE_CH3_REG (0x0324)

| 31 | 24 | 23 | 20 | 19 | 18 | 17 |
|-----|-----|-----|-----|-----|-----|-----|
| 0   | 0   | 0   | 0   | 0x0 | 0x0 |     |
|     |     |     |     |      |      | Reset |
|     |     |     |     |      |      | 0x000 |

H264_DMA_OUTLINK_DSCR_ADDR_CH3 Represents the current outlink descriptor's address for TX channel 3. (RO)

H264_DMA_OUT_DSCR_STATE_CH3 Represents the current state of the descriptor state machine for TX channel 3. (RO)

H264_DMA_OUT_STATE_CH3 Represents the current control module state machine state for TX channel 3. (RO)


Register 39.207. H264_DMA_OUT_EOF_DES_ADDR_CH3_REG (0x0328)

| 31 |     |     |     |     |     | 0 |
|----|-----|-----|-----|-----|-----|---|
|    | 0x0000000 |      | Reset |

H264_DMA_OUT_EOF_DES_ADDR_CH3 Represents the address of the inlink descriptor when the EOF bit in this descriptor is 1. (RO)
```