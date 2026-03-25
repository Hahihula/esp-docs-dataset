

```markdown
## Register 2.17. mintthresh (0x347)

| TH | 31 | 24 | 23 | (reserved) |
|----|----|----|----|------------|
|    | 0x0|     |     |            |
|    |     |     |     | 0x000000   |
| Reset |    |     |     |            |

**TH**: Configures the 8-bit level threshold of machine mode interrupts.
Note that the effective threshold level for machine mode interrupts is the maximum of `mintthresh.TH` and `mintstatus.MIL`. All machine mode pending interrupts with levels less than or equal to the effective threshold level are not allowed to preempt the execution. (R/W)

## Register 2.18. mintstatus (0xF81)

| MIL | UIL | 31 | 24 | 23 | 8 | 7 | 0 |
|-----|-----|----|----|----|---|---|---|
|     |     | 0x00|    |    |   |   |   |
|     |     |     |    |    |   |   | 0x00 |
| Reset |     |     |    |    |   |   |            |

**MIL**: Represents the active 8-bit interrupt level for current machine mode interrupt. (RO)

**UIL**: Hardwired to 0x0 as user mode interrupts are not supported. (RO)

## Register 2.19. mscratchcsW (0x348)

| MSSCRATCHCSW | 31 | 0 |
|-------------|----|---|
|             |    |   |
|             | 0x00000000 | Reset |

**MSCRATCHCSW**: Configures the MSCRATCH value by conditionally swapping its value with RS1, based on the current privilege mode and the previous privilege mode in MPP.
This is the conditional scratch swap CSR, which allows performing a scratch value swap conditionally, based on privilege mode change, in a single instruction.

When using CSRRW instruction to access this CSR, the value written into RD is either that of MSCRATCH, if MPP is different than the current privilege mode, or RS1 if MPP is the same as the current privilege mode. The MSCRATCH CSR value is updated with the original value of RS1 only if there is a privilege mode difference.

(R/W)
```