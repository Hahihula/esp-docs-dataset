

```markdown
Register 2.23. mcounthibit (0x320)

| Bit | Field   | Description                                                                 |
|-----|---------|-----------------------------------------------------------------------------|
| 14  | HPM13   | Configures the incrementing of mhpmcounter13.<br>0: Continue incrementing the mhpmcounter13 counter.<br>1: Stop incrementing the mhpmcounter13 counter.<br>(R/W) |
| 12  | (reserved) | RESERVED                                                                 |
| 10  | HPM9    | Configures the incrementing of mhpmcounter9.<br>0: Continue incrementing the mhpmcounter9 counter.<br>1: Stop incrementing the mhpmcounter9 counter.<br>(R/W) |
| 9   | (reserved) | RESERVED                                                                 |
| 8   | HPM8    | Configures the incrementing of mhpmcounter8.<br>0: Continue incrementing the mhpmcounter8 counter.<br>1: Stop incrementing the mhpmcounter8 counter.<br>(R/W) |
| 7   | (reserved) | RESERVED                                                                 |
| 3   | IR      | Configures the incrementing of the instret counter.<br>0: Continue incrementing the instret counter.<br>1: Stop incrementing the instret counter.<br>(R/W) |
| 2   | TM      | Configures the incrementing of the time counter.<br>0: Continue incrementing the time counter.<br>1: Stop incrementing the time counter.<br>(R/W) |
| 1   | CY      | Configures the incrementing of the cycle counter.<br>0: Continue incrementing the cycle counter.<br>1: Stop incrementing the cycle counter.<br>(R/W) |
| 0   | Reset   | Reset value for all bits is 0.                                             |

Register 2.24. mhpmevent8 (0x328)

| Bit | Field         | Description                                                                 |
|-----|---------------|-----------------------------------------------------------------------------|
| 5   | EVENT[4:0]    | Event selector for mhpmcounter8.<br>The only valid event value for this counter is 0x6, for conditional branch mispredictions.<br>(R/W) |

```
```plaintext
Chapter 2 High-Performance CPU

HPM13 Configures the incrementing of mhpmcounter13.
O: Continue incrementing the mhpmcounter13 counter.
1: Stop incrementing the mhpmcounter13 counter.
(R/W)

HPM9 Configures the incrementing of mhpmcounter9.
O: Continue incrementing the mhpmcounter9 counter.
1: Stop incrementing the mhpmcounter9 counter.
(R/W)

HPM8 Configures the incrementing of mhpmcounter8.
O: Continue incrementing the mhpmcounter8 counter.
1: Stop incrementing the mhpmcounter8 counter.
(R/W)

IR Configures the incrementing of the instret counter.
O: Continue incrementing the instret counter.
1: Stop incrementing the instret counter.
(R/W)

TM Configures the incrementing of the time counter.
O: Continue incrementing the time counter.
1: Stop incrementing the time counter.
(R/W)

CY Configures the incrementing of the cycle counter.
O: Continue incrementing the cycle counter.
1: Stop incrementing the cycle counter.
(R/W)
```