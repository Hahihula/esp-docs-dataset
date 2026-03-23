

```markdown
Register 4.23. GDMA_IN_ERR_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x008C+0xC0*n)

GDMA_IN_ERR_EOF_DES_ADDR_CHn Represents the address of the receive descriptor when there are some errors in the currently received data. Valid only for UHCI or PARLIO. (RO)

Register 4.24. GDMA_IN_DSCR_CHn_REG (n: 0-2) (0x0090+0xC0*n)

GDMA_INLINK_DSCR_CHn Represents the address of the next receive descriptor x+1 pointed by the current receive descriptor that is pre-read. (RO)

Register 4.25. GDMA_IN_DSCR_BFO_CHn_REG (n: 0-2) (0x0094+0xC0*n)

GDMA_INLINK_DSCR_BFO_CHn Represents the address of the current receive descriptor x that is pre-read. (RO)
```