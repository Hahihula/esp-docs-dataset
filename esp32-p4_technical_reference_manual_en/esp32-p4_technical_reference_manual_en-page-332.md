

```markdown
Register 4.113. AXI_DMA_IN_STATE_CHn_REG (n: 0-2) (0x0028+0x68*n)

AXI_DMA_INLINK_DSCR_ADDR_CHn Represents the lower 18 bits of the next receive descriptor address that is pre-read (but not processed yet). If the current receive descriptor is the last descriptor, then this field represents the address of the current receive descriptor. (RO)
AXI_DMA_IN_DSCR_STATE_CHn Reserved. (RO)
AXI_DMA_IN_STATE_CHn Reserved. (RO)

Register 4.114. AXI_DMA_IN_SUC_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x002C+0x68*n)

AXI_DMA_IN_SUC_EOF_DES_ADDR_CHn Represents the address of the receive descriptor when the EOF bit in this descriptor is 1. (RO)
```