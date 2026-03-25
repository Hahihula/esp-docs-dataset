

```markdown
Register 1.83. mtimectl (0x4010)

| Bit | Description |
|-----|-------------|
| 6   | MTIME_SAM   |
| 5   | MTIME_OVF   |
| 3-0 | reserved    |

<table><tr><td>31</td><td></td><td>6</td><td>5</td><td>4</td><td>3</td><td>0</td></tr><tr><td colspan="7">0x00000000</td></tr><tr><td></td><td></td><td>OxD</td><td></td><td>OxD</td><td>Ox1</td><td>Reset</td></tr></table>

MTIME_EN Configures whether to enable the system counter.
1: Enable
0: Disable
(R/W)

MTIME_OVF Configures the overflow bit of the system counter.
1: Represents that system counter value is maximum, that is 0xFFFFFFFFFFFFFFFF
0: Otherwise

When the counter value is 0xFFFFFFFFFFFFFFFF, which is the maximum value, then this bit is set as 1 by hardware. Software can clear this bit by writing 0 to it. Writing 1 has no effect. (R/W)

MTIME_SAM Configures the sampling mode of MTIMelo and MTIMEHI registers to allow accurate reading of the 64-bit system count. For the 64-bit system count, only one half of the read can be performed atomically. Therefore, the sampling mode allows the value of the other half to be sampled and stored in a buffer, and upon the next read of the other half, the sampled value from this buffer is retrieved instead of the actual counter.

0x0: No sampling (Default)
0x1: Sample upper half of the system count on reading MTIMELO
0x2: Sample lower half of the system count on reading MTIMEHI
0x3: Sample the other half of the system count on reading MTIMELO or MTIMEHI
(R/W)

Register 1.84. mtimeelo (0xBFF8)

| Bit | Description |
|-----|-------------|
| 31  | MTIMELO     |

<table><tr><td>31</td><td></td><td>0</td></tr><tr><td colspan="3">0x00000000</td></tr><tr><td></td><td></td><td>Reset</td></tr></table>

MTIMELO Represents the current value of the lower 32 bits of the system counter. (RO)
```