

```markdown
Register 6.55. DMA2D_IN_SUC_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x0528+0x100*n)

DMA2D_IN_SUC_EOF_DES_ADDR_CHn Represents the address of the receive descriptor when the eof bit in this descriptor is 1. (RO)


Register 6.56. DMA2D_IN_ERR_EOF_DES_ADDR_CHn_REG (n: 0-2) (0x052C+0x100*n)

DMA2D_IN_ERR_EOF_DES_ADDR_CHn Represents the address of the receive descriptor when there are some errors in the currently received data. Valid only for JPEG. (RO)


Register 6.57. DMA2D_IN_DSCR_CHn_REG (n: 0-2) (0x0530+0x100*n)

DMA2D_INLINK_DSCR_CHn Represents the address of the next receive descriptor pointed by the current receive descriptor that is pre-read. (RO)
```