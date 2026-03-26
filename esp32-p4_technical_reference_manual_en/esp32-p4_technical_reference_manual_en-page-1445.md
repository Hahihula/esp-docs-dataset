

```markdown
Register 25.12. AES_STATE_REG (0x004C)

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
Register 25.13. AES_CONTINUE_OP_REG (0x00A8)

AES_CONTINUE_OP Configures whether to continue AES operation.

O: No effect
1: Continue
(WO)
```