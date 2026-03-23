

```markdown
Register 21.2. SHA_CONTINUE_REG (0x0014)

SHA_CONTINUE Write 1 to continue Typical SHA calculation. (WO)
```

```markdown
Register 21.3. SHA_BUSY_REG (0x0018)

SHA_BUSY_STATE Indicates the states of SHA accelerator. (RO) 1'h0: idle 1'h1: busy
```

```markdown
Register 21.4. SHA_DMA_START_REG (0x001C)

SHA_DMA_START Write 1 to start DMA-SHA calculation. (WO)
```

```markdown
Register 21.5. SHA_DMA_CONTINUE_REG (0x0020)

SHA_DMA_CONTINUE Write 1 to continue DMA-SHA calculation. (WO)
```