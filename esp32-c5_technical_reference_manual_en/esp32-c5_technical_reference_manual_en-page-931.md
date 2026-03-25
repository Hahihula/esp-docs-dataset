

```markdown
## Register 26.8. SHA_DATE_REG (0x002C)

SHA_DATE Version control register. (R/W)


## Register 26.9. SHA_MODE_REG (0x0000)

SHA_MODE Configures the SHA algorithm.
O: SHA-1
1: SHA-224
2: SHA-256
3 ~ 7: invalid value
(R/W)


## Register 26.10. SHA_DMA_BLOCK_NUM_REG (0x000C)

SHA_DMA_BLOCK_NUM Configures the DMA-SHA block number. (R/W)


## Register 26.11. SHA_H_n_REG (n: 0-7) (0x0040+4*n)

SHA_H_n Represents the nth 32-bit piece of the Hash value. (R/W)
```