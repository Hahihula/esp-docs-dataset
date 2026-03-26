

```markdown
Register 4.120. AXI_DMA_OUT_STATE_CHn_REG (n: 0-2) (0x0160+0x68*n)

AXI_DMA_OUTLINK_DSCR_ADDR_CHn Represents the lower 18 bits of the next transmit descriptor address that is pre-read (but not processed yet). If the current transmit descriptor is the last descriptor, then this field represents the address of the current transmit descriptor. (RO)

AXI_DMA_OUT_DSCR_STATE_CHn Reserved. (RO)

AXI_DMA_OUT_STATE_CHn Reserved. (RO)


Register 4.121. AXI_DMA_OUT_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x0164+0x68*n)

AXI_DMA_OUT_EOF_DES_ADDR_CHn Represents the address of the transmit descriptor when the EOF bit in this descriptor is 1. (RO)
```