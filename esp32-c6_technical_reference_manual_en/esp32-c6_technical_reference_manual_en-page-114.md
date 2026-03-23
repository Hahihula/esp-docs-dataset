

```markdown
Register 3.10. mip (0x344)

IP   Configures the pending status of the interrupt.
    O: Not pending
    1: Pending
    (R/W)
```

```markdown
Register 3.11. mcycle (0xB00)

MCYCLE   Configures the lower 32 bits of the clock cycle counter. (R/W)
```

```markdown
Register 3.12. minstret (0xB02)

MINSTRET   Configures the lower 32 bits of the instruction counter. (R/W)
```

```markdown
Register 3.13. mhpmcounter(n: 0 - 12) (0xB00+n)

MHPMCOUNTERn   Configures the lower 32 bits of the performance counter n. (R/W)
```