

```markdown
## Register 23.8. SHA_DATE_REG (0x002C)

| 31 | 30 | 29 | [Reserved] |
|----:|----:|----:|------------|
|   0 |   0 | Ox20190402 | Reset |

SHA_DATE Version control register. (R/W)


## Register 23.9. SHA_MODE_REG (0x0000)

| 31 | [Reserved] | 3 | 2 | 1 | 0 |
|----:|------------:|---:|---:|---:|---|
|   0 |            Ox0 |   0 |   0 |   0 | Reset |

SHA_MODE Configures the SHA algorithm.
- O: SHA-1
- 1: SHA-224
- 2: SHA-256

(R/W)


## Register 23.10. SHA_DMA_BLOCK_NUM_REG (0x000C)

| 31 | [Reserved] | 6 | 5 | 0 |
|----:|------------:|---:|---:|---|
|   0 |            Ox0 |   0 |   0 | Reset |

SHA_DMA_BLOCK_NUM Configures the DMA-SHA block number. (R/W)


## Register 23.11. SHA_H_n_REG (n: 0-7) (0x0040+4*n)

| 31 |
|----|
| Ox000000 |

SHA_H_n Represents the nth 32-bit piece of the Hash value. (R/W)
```