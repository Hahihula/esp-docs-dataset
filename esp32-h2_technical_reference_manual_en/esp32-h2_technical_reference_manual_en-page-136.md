

```markdown
Register 3.28. GDMA_OUT_STATE_CHn_REG (n: 0-2) (0x00E4+0xC0*n)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|--------------------------------|-----------------------------------------------------------------------------|
| 31        |                                |                                                                             |
| 23..18    | GDMA_OUT_STATE_CHO             |                                                                             |
| 17..16    | GDMA_OUT_DSCR_STATE_CHO        |                                                                             |
| 15..0     | GDMA_OUTLINK_DSCR_ADDR_CHO     |                                                                             |

GDMA_OUTLINK_DSCR_ADDR_CHn Represents the lower 18 bits of the address of the next transmit descriptor that is pre-read (but not processed yet). If the current transmit descriptor is the last descriptor, then this field represents the address of the current transmit descriptor. (RO)

GDMA_OUT_DSCR_STATE_CHn Reserved. (RO)

GDMA_OUT_STATE_CHn Reserved. (RO)


Register 3.29. GDMA_OUT_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x00E8+0xC0*n)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|--------------------------------|-----------------------------------------------------------------------------|
| 31..0     | GDMA_OUT_EOF_DES_ADDR_CHO      |                                                                             |

GDMA_OUT_EOF_DES_ADDR_CHn Represents the address of the transmit descriptor when the EOF bit in this descriptor is 1. (RO)
```