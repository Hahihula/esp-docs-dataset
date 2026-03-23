

```markdown
Register 1.5. mstatus (0x300)

| 31 | 22 | 21 | 20 | 13 | 12 | 11 | 10 | 8 | 7 | 6 | 4 | 3 | 2 | 0 |
|-----|-----|-----|-----|-----|-----|-----|-----|----|----|----|----|----|----|----|
|     | TW  |     |     |     | MPP | (reserved) | MPIE | (reserved) | MIE | (reserved) | Reset |
| 0x000 | 0   | 0x00 | 0x0 | 0x0 | O   | 0x0 | 0   | 0   | 0x0 | 0   |      |

MIE Global machine mode interrupt enable. (R/W)

MPIE Machine previous interrupt enable (before trap). (R/W)

MPP Machine previous privilege mode (before trap). (R/W)
Possible values:
* 0x0: User mode
* 0x3: Machine mode

Note: Only lower bit is writable. Write to the higher bit is ignored as it is directly tied to the lower bit.

TW Timeout wait. (R/W)
If this bit is set, executing WFI (Wait-for-Interrupt) instruction in User mode will cause illegal instruction exception.
```