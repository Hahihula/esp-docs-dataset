

```markdown
Register 1.18. mintstatus (0xFB1)

| 31 | MIL | 24 | 23 | (reserved) | UIL | 7 | 0 |
|-----|-----|----|----|------------|-----|---|---|
|     |     |    |    |            |     |   |   |
| 0x00 |      | 0x0000 |      | 0x00       |

MIL Represents the active 8-bit interrupt level for current machine mode interrupt. (RO)
UIL Represents the active 8-bit interrupt level for current user mode interrupt. (RO)

Register 1.19. msratchcsw (0x348)

| 31 | MSCRATCHCSW | 0 |
|----|-------------|---|
|    | 0x00000000   |

MSCRATCHCSW Configures the MSCRATCH value by conditionally swapping its value with RS1, based on the current privilege mode and the previous privilege mode in MPP. This is the conditional scratch swap CSR, which allows performing a scratch value swap conditionally, based on privilege mode change, in a single instruction.

When using CSRRW instruction to access this CSR, the value written into RD is either that of MSCRATCH, if MPP is different than the current privilege mode, or RS1 if MPP is the same as the current privilege mode. The MSCRATCH CSR value is updated with the original value of RS1 only if there is a privilege mode difference.
(R/W)
```