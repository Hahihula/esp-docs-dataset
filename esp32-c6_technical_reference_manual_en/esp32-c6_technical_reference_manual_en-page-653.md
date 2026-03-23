

```markdown
Register 19.11. AES_DMA_EXIT_REG (0x00B8)

AES_DMA_EXIT   Configures whether or not to exit AES operation.
               O: No effect
               1: Exit
               Only valid for DMA-AES operation. (WO)
```

```markdown
Register 19.12. AES_INT_CLEAR_REG (0x00AC)

AES_INT_CLEAR  Configures whether or not to clear AES interrupt.
               O: No effect
               1: Clear
               (WO)
```

```markdown
Register 19.13. AES_INT_ENA_REG (0x00B0)

AES_INT_ENA    Configures whether or not to enable AES interrupt.
               O: Disable
               1: Enable
               (R/W)
```