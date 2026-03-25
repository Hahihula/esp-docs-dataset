

```markdown
## Register 21.8. SHA_DATE_REG (0x002C)

SHA_DATE Version control register. (R/W)


| 31 | 30 | 29 | [Reserved] |
|----:|----:|----:|------------|
|   0 |   0 |     |            |

Reset value: `0x20201229`
```

```markdown
## Register 21.9. SHA_MODE_REG (0x0000)

SHA_MODE Configures the SHA algorithm.

- O: SHA-1
- 1: SHA-224
- 2: SHA-256
- 3 ~ 7: invalid value

(R/W)


| 31 | [Reserved] | ... | 3 | 2 | 1 | 0 |
|----:|------------|-----|---:|---:|---:|---:|
|   0 |            |     |   0 |   0 |   0 | Ox0 |

Reset value: `0x0`
```

```markdown
## Register 21.10. SHA_DMA_BLOCK_NUM_REG (0x000C)

SHA_DMA_BLOCK_NUM Configures the DMA-SHA block number. (R/W)


| 31 | [Reserved] | ... | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----:|------------|-----|---:|---:|---:|---:|---:|---:|---:|
|   0 |            |     |   0 |   0 |   0 |   0 |   0 | Ox0 |

Reset value: `0x0`
```

```markdown
## Register 21.11. SHA_H_n_REG (n: 0-7) (0x0040+4*n)

SHA_H_n Represents the nth 32-bit piece of the Hash value. (R/W)


| 31 | [Reserved] |
|----:|------------|
|   0 |            |

Reset value: `0x000000`
```

```markdown
Espressif Systems    792

ESP32-C61 TRM (Pre-release v0.5)

Submit Documentation Feedback PRELIMINARY
```