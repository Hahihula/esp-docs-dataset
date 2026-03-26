

```markdown
Register 1.33. mcounthibit (0x320)

| 31 | 14 | 13 | 12 | 10 | 9 | 8 | 7 | 3 | 2 | 1 | 0 |
|----:|----:|----:|----:|----:|---:|---:|---:|---:|---:|---:|---:|
|    | HPM13 | (reserved) | HPM9 | HPM8 | (reserved) | IR | TM | CY |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

HPM13 Configures the incrementing of mhpcounter13.
O: Continue incrementing the mhpcounter13 counter.
1: Stop incrementing the mhpcounter13 counter.
(R/W)

HPM9 Configures the incrementing of mhpcounter9.
O: Continue incrementing the mhpcounter9 counter.
1: Stop incrementing the mhpcounter9 counter.
(R/W)

HPM8 Configures the incrementing of mhpcounter8.
O: Continue incrementing the mhpcounter8 counter.
1: Stop incrementing the mhpcounter8 counter.
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

Register 1.34. mhpmevent8 (0x328)

| 31 | 5 | 4 | 0 |
|----:|---:|---:|---:|
|    | EVENT[4:0] |

```markdown
EVENT[4:0] Event selector for mhpcounter8.
The only valid event value for this counter is 0x6, for conditional branch mispredictions.
(R/W)
```

Espressif Systems

87

ESP32-P4 TRM

Submit Documentation Feedback PRELIMINARY