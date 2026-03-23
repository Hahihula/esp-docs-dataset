

```markdown
Register 4.30. GDMA_OUT_EOF_BFR_DES_ADDR_CHn_REG (n: 0-2) (0x00EC+0xC0*n)

GDMA_OUT_EOF_BFR_DES_ADDR_CHn   Represents the address of the transmit descriptor before the last transmit descriptor. (RO)

Register 4.31. GDMA_OUT_DSCR_CHn_REG (n: 0-2) (0x00F0+0xC0*n)

GDMA_OUTLINK_DSCR_CHn   Represents the address of the next transmit descriptor y+1 pointed by the current transmit descriptor that is pre-read. (RO)

Register 4.32. GDMA_OUT_DSCR_BFO_CHn_REG (n: 0-2) (0x00F4+0xC0*n)

GDMA_OUTLINK_DSCR_BFO_CHn   Represents the address of the current transmit descriptor y that is pre-read. (RO)
```