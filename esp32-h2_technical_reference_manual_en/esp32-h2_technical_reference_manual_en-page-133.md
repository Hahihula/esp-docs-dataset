

```markdown
Register 3.21. GDMA_IN_STATE_CHn_REG (n: 0-2) (0x0084+0xC0*n)

| 31 | 23 | 22 | 20 | 19 | 18 | 17 |
|----|----|----|----|----|----|----|
| 0  | 0  | 0  | 0  | 0  | 0  |    |
|    |    |    |    |    |    | Reset |

GDMA_INLINK_DSCR_ADDR_CHn Represents the lower 18 bits of the address of the next receive descriptor that is pre-read (but not processed yet). If the current receive descriptor is the last descriptor, then this field represents the address of the current receive descriptor. (RO)

GDMA_IN__DSCR_STATE_CHn Reserved. (RO)

GDMA_IN_STATE_CHn Reserved. (RO)

Register 3.22. GDMA_IN_SUC_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x0088+0xC0*n)

| 31 |    |
|----|-----|
|    | 0x000000 |
|    | Reset |

GDMA_IN_SUC_EOF_DES_ADDR_CHn Represents the address of the receive descriptor when the EOF bit in this descriptor is 1. (RO)
```