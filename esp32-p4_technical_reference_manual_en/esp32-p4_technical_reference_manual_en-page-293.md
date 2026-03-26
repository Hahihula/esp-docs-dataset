

```markdown
Register 4.56. AHB_DMA_OUT_EOF_BFR_DESC_ADDR_CHn_REG (n: 0-2) (0x00EC+0xC0*n)

| 31 | 0 |
|-----|----|
|     |    |
| 0x000000 | Reset |

AHB_DMA_OUT_EOF_BFR_DESC_ADDR_CHn Represents the address of the transmit descriptor before the last transmit descriptor. (RO)


Register 4.57. AHB_DMA_OUT_DSCR_CHn_REG (n: 0-2) (0x00FO+0xC0*n)

| 31 | 0 |
|-----|----|
|     |    |
|      | Reset |

AHB_DMA_OUTLINK_DSCR_CHn Represents the address of the next transmit descriptor y+1 pointed by the current transmit descriptor that is pre-read. (RO)


Register 4.58. AHB_DMA_OUT_DSCR_BFO_CHn_REG (n: 0-2) (0x00F4+0xC0*n)

| 31 | 0 |
|-----|----|
|     |    |
|      | Reset |

AHB_DMA_OUTLINK_DSCR_BFO_CHn Represents the address of the current transmit descriptor y that is pre-read. (RO)
```