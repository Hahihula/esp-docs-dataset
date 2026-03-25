

```markdown
## Register 3.38. AHB_DMA_OUT_STATE_CHn_REG (n: 0-1) (0x00E4+0xC0*n)

| Bit Range | Field Name                          |
|-----------|--------------------------------------|
| 31        | (reserved)                          |
| 23..17    | AHB_DMA_OUT_STATE_CHn               |
| 16..0     | AHB_DMA_OUT_DSCR_STATE_CHn          |

AHB_DMA_OUTLINK_DSCR_ADDR_CHn Represents the lower 18 bits of the next transmit descriptor address that is pre-read (but not processed yet). If the current transmit descriptor is the last descriptor, then this field represents the address of the current transmit descriptor. (RO)

AHB_DMA_OUT_DSCR_STATE_CHn Reserved. (RO)

AHB_DMA_OUT_STATE_CHn Reserved. (RO)


## Register 3.39. AHB_DMA_OUT_EOF_DES_ADDR_CHn_REG (n: 0-1) (0x00E8+0xC0*n)

| Bit Range | Field Name                          |
|-----------|--------------------------------------|
| 31..0     | (reserved, all bits reset to 0x00000000) |

AHB_DMA_OUT_EOF_DES_ADDR_CHn Represents the address of the transmit descriptor when the EOF bit in this descriptor is 1. (RO)
```