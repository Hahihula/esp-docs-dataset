

```markdown
Register 2.24. GDMA_OUT_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x00E8+192*n)

GDMA_OUT_EOF_DES_ADDR_CHn  This register stores the address of the transmit descriptor when the EOF bit in this descriptor is 1. (RO)

Register 2.25. GDMA_OUT_EOF_BFR_DES_ADDR_CHn_REG (n: 0-2) (0x00EC+192*n)

GDMA_OUT_EOF_BFR_DES_ADDR_CHn  This register stores the address of the transmit descriptor before the last transmit descriptor. (RO)

Register 2.26. GDMA_OUT_DSCR_CHn_REG (n: 0-2) (0x00F0+192*n)

GDMA_OUTLINK_DSCR_CHn  Represents the address of the next transmit descriptor y+1 pointed by the current transmit descriptor that is pre-read. (RO)
```