

```markdown
Register 4.49. AHB_DMA_IN_ERR_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x008C+0xC0*n)

AHB_DMA_IN_ERR_EOF_DES_ADDR_CHn   Represents the address of the receive descriptor when there are some errors in the currently received data. Valid only for UHCI. (RO)

Register 4.50. AHB_DMA_IN_DSCR_CHn_REG (n: 0-2) (0x0090+0xC0*n)

AHB_DMA_INLINK_DSCR_CHn   Represents the address of the next receive descriptor x+1 pointed by the current receive descriptor that is pre-read. (RO)

Register 4.51. AHB_DMA_IN_DSCR_BFO_CHn_REG (n: 0-2) (0x0094+0xC0*n)

AHB_DMA_INLINK_DSCR_BFO_CHn   Represents the address of the current receive descriptor x that is pre-read. (RO)
```