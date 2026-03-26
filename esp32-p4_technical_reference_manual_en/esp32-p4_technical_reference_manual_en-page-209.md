

```markdown
## Register 3.6. mscratch (0x340)

MSCRATCH

| Bit | Description |
|-----|-------------|
| 31  |             |
|     | `0x00000000` Reset |

**MSCRATCH** Contains machine scratch information for custom use. (R/W)


## Register 3.7. mepc (0x341)

MEPC

| Bit | Description |
|-----|-------------|
| 31  |             |
|     | `0x00000000` Reset |

**MEPC** Configures the machine trap/exception program counter. This is automatically updated with address of the instruction which was about to be executed while CPU encountered the most recent trap. (R/W)


## Register 3.8. mcause (0x342)

Interrupt Flag | (reserved) | Exception Code
| Bit 31-30 |           |              |
|-----------|-----------|--------------|
| O         | `0x000000` | `0x00` Reset |

**Exception Code** This field is automatically updated with unique ID of the most recent exception or interrupt due to which CPU entered trap. Possible exception IDs are:
- 0x2: Illegal instruction
- 0x3: Hardware breakpoint/watchpoint or EBREAK
- 0x6: Misaligned atomic instructions

Note: Exception ID 0x0 (instruction access misaligned) is not present because CPU always masks the lowest bit of the address during instruction fetch. (R/W)

**Interrupt Flag** This flag is automatically updated when CPU enters trap. If this is found to be set, it indicates that the latest trap occurred due to an interrupt. For exceptions it remains unset. (R/W)
```