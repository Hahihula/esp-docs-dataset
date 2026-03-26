

```markdown
| Name          | Description                                                                 | Address   | Access |
|---------------|-----------------------------------------------------------------------------|-----------|--------|
| msip          | Core-local machine software interrupt pending register                      | 0x0000    | R/W    |
| mtimecmplo    | Lower 32 bits of the core-local machine timer compare value                | 0x4000    | R/W    |
| mtimecmphi    | Higher 32-bit core-local machine timer compare value                       | 0x4004    | R/W    |
| mtimeloadlo   | Lower 32 bits of core-local machine timer load value                       | 0x4008    | R/W    |
| mtimeloadhi   | Higher 32 bits of core-local machine timer load value                      | 0x400C    | R/W    |
| mtimectl      | Core-local machine timer interrupt control/status register                 | 0x4010    | R/W    |
| mtimelo       | Lower 32 bits of core-local timer counter value                            | 0xBFF8    | RO     |
| mtimehi       | Higher 32 bits core-local timer counter value                              | 0xBFFC    | RO     |

### 1.9.3.6 Register Description

The addresses in this section are relative to CPU sub-system base address provided in Figure 7.3-1 in Chapter 7 System and Memory.

#### Register 1.100. msip (0x0000)

MSIP Configures the pending status of the machine software interrupt.
O: Not pending
1: Pending
(R/W)

#### Register 1.101. mtimecmplo (0x4000)

MTIMECMPLO Represents the value to compare with the lower 32 bits of the system counter. (R/W)
```