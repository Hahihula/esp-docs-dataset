
```markdown
Register 1.16. uie (0x004)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | UXIE[31:8]                                                                  |
|     |                                                                             |
| 7   | (reserved)                                                                 |
| 6   | UXIE[6:5]                                                                   |
| 5   | UTIE                                                                         |
| 4   | UXIE[2:1]                                                                    |
| 3   | (reserved)                                                                  |
| 2   | UXIE[0]                                                                     |
| 1   | USIE                                                                        |
| 0   |                                                                             |

USIE Write 1 to enable the user software interrupt. (R/W)
UTIE Write 1 to enable the user timer interrupt. (R/W)
UXIE Write 1 to enable the 28 external interrupts delegated to U mode. (R/W)

Register 1.17. utvec (0x005)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | BASE                                                                       |
|     |                                                                             |
| 7   | (reserved)                                                                 |
| 6   | MODE                                                                        |
| 5   |                                                                             |
| 4   |                                                                             |
| 3   |                                                                             |
| 2   |                                                                             |
| 1   |                                                                             |
| 0   |                                                                             |

MODE Represents if user mode interrupts are vectored. Only vectored mode 0x1 is available. (RO)
BASE Configures the higher 24 bits of trap vector base address aligned to 256 bytes. (R/W)

Register 1.18. uscratch (0x040)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | USCRATCH                                                                    |
|     |                                                                             |
| 7   | 0                                                                           |
| 6   | 0                                                                           |
| 5   | 0                                                                           |
| 4   | 0                                                                           |
| 3   | 0                                                                           |
| 2   | 0                                                                           |
| 1   | 0                                                                           |
| 0   |                                                                             |

USCRATCH Configures user scratch information for custom use. (R/W)

Register 1.19. uepc (0x041)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | UEPC                                                                        |
|     |                                                                             |
| 7   | 0                                                                           |
| 6   | 0                                                                           |
| 5   | 0                                                                           |
| 4   | 0                                                                           |
| 3   | 0                                                                           |
| 2   | 0                                                                           |
| 1   | 0                                                                           |
| 0   |                                                                             |

UEPC Configures the user trap program counter. This is automatically updated with address of the instruction which was about to be executed in User mode while CPU encountered the most recent user mode interrupt. (R/W)
```