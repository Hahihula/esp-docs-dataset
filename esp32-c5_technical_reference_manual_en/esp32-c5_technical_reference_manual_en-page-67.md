

```markdown
Chapter 2 High-Performance CPU

Register 2.25. mhpmevent9 (0x329)

EVENT[4:0] Event selector for mhpmcounter9.
The only valid event value for this counter is 0x7, for conditional branch instructions.
(R/W)

Register 2.26. mhpmevent13 (0x32D)

EVENT[4:0] Event selector for mhpmcounter13.
The only valid event value for this counter is 0xB, for store instructions.
(R/W)

Register 2.27. mcycle (0xB00)

MCYCLE Represents the lower 32 bits of the machine mode cycle counter. (R/W)

Register 2.28. minstret (0xB02)

MINSTRET Represents the lower 32 bits of the machine instructions retired counter. (R/W)
```