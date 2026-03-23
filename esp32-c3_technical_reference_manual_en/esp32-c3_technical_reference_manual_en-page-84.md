

```markdown
Register 2.17. GDMA_IN_SUC_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x0088+192*n)

GDMA_IN_SUC_EOF_DES_ADDR_CHn   This register stores the address of the receive descriptor when the EOF bit in this descriptor is 1. (RO)

Register 2.18. GDMA_IN_ERR_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x008C+192*n)

GDMA_IN_ERR_EOF_DES_ADDR_CHn   This register stores the address of the receive descriptor when there are some errors in current receiving data. Only used when peripheral is UHCI0. (RO)

Register 2.19. GDMA_IN_DSCR_CHn_REG (n: 0-2) (0x0090+192*n)

GDMA_INLINK_DSCR_CHn   Represents the address of the next receive descriptor x+1 pointed by the current receive descriptor that is pre-read. (RO)
```