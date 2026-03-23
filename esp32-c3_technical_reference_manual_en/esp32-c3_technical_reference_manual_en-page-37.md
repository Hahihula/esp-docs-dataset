

```markdown
Register 1.7. mtvec (0x305)

| 31 | 8 | 7 | (reserved) | 2 | 1 | 0 |
|-----|----|----|------------|---|---|---|
|     |    |    |            |   |   |   |
| 0x000000 | 0x00 | 0x1 | Reset |

MODE Only vectored mode 0x1 is available. (RO)
BASE Higher 24 bits of trap vector base address aligned to 256 bytes. (R/W)

Register 1.8. mscratch (0x340)

| 31 | 0 |
|-----|----|
|     |    |

| 0x00000000 | Reset |

MSCRATCH Machine scratch register for custom use. (R/W)

Register 1.9. mepc (0x341)

| 31 | 0 |
|-----|----|
|     |    |

| 0x00000000 | Reset |

MEPC Machine trap/exception program counter. (R/W)
This is automatically updated with address of the instruction which was about to be executed
while CPU encountered the most recent trap.
```