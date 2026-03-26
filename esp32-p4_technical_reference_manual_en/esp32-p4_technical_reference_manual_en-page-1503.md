

```markdown
Register 29.4. SHA_DMA_BLOCK_NUM_REG (0x000C)

SHA_DMA_BLOCK_NUM Configures the DMA-SHA block number. (R/W)
```

```markdown
Register 29.5. SHA_START_REG (0x0010)

SHA_START Write 1 to start Typical SHA calculation. (WO)
```

```markdown
Register 29.6. SHA_CONTINUE_REG (0x0014)

SHA_CONTINUE Write 1 to continue Typical SHA calculation. (WO)
```

```markdown
Register 29.7. SHA_BUSY_REG (0x0018)

SHA_BUSY_STATE Represents the states of SHA accelerator.
O: idle
1: busy
(RO)
```