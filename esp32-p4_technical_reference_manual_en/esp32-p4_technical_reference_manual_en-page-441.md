

```markdown
Register 6.20. DMA2D_IN_LINK_ADDR_CHn_REG (n: 0-2) (0x0520+0x100*n)

DMA2D_INLINK_ADDR_CHn Represents the first receive descriptor's address. (R/W)


Register 6.21. DMA2D_IN_ARB_CHn_REG (n: 0-2) (0x0540+0x100*n)

DMA2D_IN_ARB_TOKEN_NUM_CHn Configures the weight (i.e the number of tokens) of RX channel n.
Value range: 0 ~ 15. (R/W)

DMA2D_IN_ARB_PRIORITY_CHn Configures the lower two bits of RX channel n priority.
Together with DMA2D_IN_ARB_PRIORITY_H_CHn, this field forms a 4-bit priority value for TX channel n, ranging from 0 (lowest) to 15 (highest). (R/W)

DMA2D_IN_ARB_PRIORITY_H_CHn Configures the higher two bits of TX channel n priority.
Together with DMA2D_IN_ARB_PRIORITY_CHn, this field forms a 4-bit priority value for TX channel n, ranging from 0 (lowest) to 15 (highest). (R/W)
```