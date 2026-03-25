

```markdown
Register 22.12. AES_STATE_REG (0x004C)

AES_STATE Represents the working status of the AES accelerator.

In Typical AES working mode:
O: IDLE
1: WORK
2: No effect
3: No effect

In DMA-AES working mode:
O: IDLE
1: WORK
2: DONE
3: No effect
(RO)
```

```markdown
Register 22.13. AES_INT_CLEAR_REG (0x00AC)

AES_INT_CLEAR Write 1 to clear the AES interrupt. (WT)
```

```markdown
Register 22.14. AES_INT_ENA_REG (0x00B0)

AES_INT_ENA Write 1 to enable the AES interrupt. (R/W)
```