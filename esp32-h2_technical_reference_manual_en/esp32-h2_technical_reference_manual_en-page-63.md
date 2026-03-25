

```markdown
Register 1.30. UTIMECTL (0x1C04)

UTIE Write 1 to enable the user timer interrupt. (R/W)
UTIP Represents the pending status of the user timer interrupt. (RO)
UTOF Configures whether the user timer overflows.
    0: Not overflow
    1: Overflow
    (R/W)

Register 1.31. UTIME (0x1C08)

UTIME Represents the read-only 64-bit CLINT timer counter value. (RO)

Register 1.32. UTIMECMP (0x1C10)

UTIMECMP Configures the 64-bit user timer compare value. (R/W)
```