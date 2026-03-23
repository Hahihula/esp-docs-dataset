

```markdown
Register 1.30. UTIMECTL (0x1C04)

| Bit | Field | Description |
|-----|-------|-------------|
| 31  | reserved |             |
| 4   | UTF    | Configures whether the user timer overflows.<br>0: Not overflow<br>1: Overflow (R/W) |
| 3   | UTIP   | Represents the pending status of the user timer interrupt. (RO) |
| 2   | UTIE   | Write 1 to enable the user timer interrupt. (R/W) |
| 1-0 | reserved |             |

Register 1.31. UTIME (0x1C08)

| Bit Range     | Field      | Description |
|---------------|------------|-------------|
| 63:32         | UTIME[63:32]| o           |
|               |            | Reset       |
| 31:0          | UTIME[31:0]| o           |
|               |            | Reset       |

UTIME Represents the read-only 64-bit CLINT timer counter value. (RO)

Register 1.32. UTIMECMP (0x1C10)

| Bit Range     | Field        | Description |
|---------------|--------------|-------------|
| 63:32         | UTIMECMP[63:32]| o           |
|               |              | Reset       |
| 31:0          | UTIMECMP[31:0]| o           |
|               |              | Reset       |

UTIMECMP Configures the 64-bit user timer compare value. (R/W)
```