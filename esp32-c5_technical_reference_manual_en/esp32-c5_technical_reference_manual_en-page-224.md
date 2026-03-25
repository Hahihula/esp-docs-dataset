

```markdown
Register 5.31. AHB_DMA_IN_STATE_CHn_REG (n: 0-2) (0x0084+0xC0*n)

| Bit Range | Field Name                     |
|-----------|--------------------------------|
| 31        |                                |
|           |                                |
| 23..22    |                                |
| 20..19    |                                |
| 18..17    |                                |
| 16..0     | (reserved)                    |
|           | O                             |
|           | Reset                         |

AHB_DMA_INLINK_DSCR_ADDR_CHn Represents the lower 18 bits of the next receive descriptor address that is pre-read (but not processed yet). If the current receive descriptor is the last descriptor, then this field represents the address of the current receive descriptor. (RO)

AHB_DMA_IN_DSCR_STATE_CHn Reserved. (RO)

AHB_DMA_IN_STATE_CHn Reserved. (RO)


Register 5.32. AHB_DMA_IN_SUC_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x0088+0xC0*n)

| Bit Range | Field Name                     |
|-----------|--------------------------------|
| 31        |                                |
|           |                                |
|           |                                |
|           |                                |
|           |                                |
|           |                                |
|           |                                |
|           |                                |
|           | O                              |
|           | Reset                         |

AHB_DMA_IN_SUC_EOF_DES_ADDR_CHn Represents the address of the receive descriptor when the EOF bit in this descriptor is 1. (RO)
```