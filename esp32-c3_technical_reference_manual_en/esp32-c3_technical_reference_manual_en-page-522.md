

```markdown
Register 21.10. SHA_DMA_BLOCK_NUM_REG (0x000C)

SHA_DMA_BLOCK_NUM    Defines the DMA-SHA block number. (R/W)

Register 21.11. SHA_H_n_REG (n: 0-7) (0x0040+4*n)

SHA_H_n   Stores the nth 32-bit piece of the Hash value. (R/W)

Register 21.12. SHA_M_n_REG (n: 0-15) (0x0080+4*n)

SHA_M_n   Stores the nth 32-bit piece of the message. (R/W)
```