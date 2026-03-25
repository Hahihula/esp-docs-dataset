

```markdown
Register 1.22. ustatus (0x000)

Continued from the previous page...

MPIE Represents the machine previous interrupt enable status (before trap).
O: Disabled
1: Enabled
(RO)

UPIE Represents the user previous interrupt enable status (before trap).
O: Disabled
1: Enabled
(RO)

MIE Represents the global machine interrupt enable status.
O: Disabled
1: Enabled
(RO)

UIE Represents the global user mode interrupt enable status.
O: Disabled
1: Enabled
(RO)

Register 1.23. utvec (0x005)
```
```markdown
| 31 | 6 | 5 | 2 | 1 | 0 |
|-----|---|----|----|----|----|
|     |    |     |     |     | Reset |
| 0x000000 | 0x00 | 0x3 |
```
```markdown
BASE Configures the higher 26 bits of exception and non-vectored user mode interrupt base address aligned to 64 bytes.(R/W)

MODE Represents whether user mode interrupts are operating in CLIC mode or vectored/non-vectored CLINT mode. Only CLIC mode 0x3 is available. (RO)
```