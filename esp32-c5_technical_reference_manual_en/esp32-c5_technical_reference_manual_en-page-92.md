

```markdown
| Name           | Description                                                                 | Address   | Access |
|----------------|-----------------------------------------------------------------------------|-----------|--------|
| mtimecmplo     | Lower 32 bits of the core-local machine timer compare value                 | 0x4000    | R/W    |
| mtimecmphi     | Higher 32-bit core-local machine timer compare value                        | 0x4004    | R/W    |
| mtimeloadlo    | Lower 32 bits of core-local machine timer load value                         | 0x4008    | R/W    |
| mtimeloadhi    | Higher 32 bits of core-local machine timer load value                        | 0x400C    | R/W    |
| mtimectl       | Core-local machine timer interrupt control/status register                   | 0x4010    | R/W    |
| mtimelo        | Lower 32 bits of core-local timer counter value                              | 0xBFF8    | RO     |
| mtimehi        | Higher 32 bits core-local timer counter value                                | 0xBFFC    | RO     |

### 2.8.3.6 Register Description

The addresses in this section are relative to the CPU sub-system base address, i.e., 0x20000000.

#### Register 2.68. msip (0x0000)

```markdown
| 31 | reserved                                                                 | MSIP |
|----|---------------------------------------------------------------------------|------|
|    | 0                                                                         |      |
|    | 0x00000000                                                                | Reset|
```

**MSIP** Configures the pending status of the machine software interrupt.
- 0: Not pending
- 1: Pending
(R/W)

#### Register 2.69. mtimecmplo (0x4000)

```markdown
| 31                                                                 | MTIMECMPLO |
|--------------------------------------------------------------------|------------|
| OxFFFFFFFF                                                      | Reset      |
```

**MTIMECMPLO** Represents the value to compare with the lower 32 bits of the system counter. (R/W)
```