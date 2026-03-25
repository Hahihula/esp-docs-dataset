

```markdown
Register 1.33. mcounthhibit (0x320)

| Bit | Field   | Description                                                                 |
|-----|---------|-----------------------------------------------------------------------------|
| 31  |         | (reserved)                                                                  |
| 14  | HPM13   | Configures the incrementing of mhpmcounter13.                               |
|     |         | 0: Continue incrementing the mhpmcounter13 counter.                         |
|     |         | 1: Stop incrementing the mhpmcounter13 counter.                             |
|     | (R/W)   |                                                                             |
| 12  | HPM9    | Configures the incrementing of mhpmcounter9.                                |
|     |         | 0: Continue incrementing the mhpmcounter9 counter.                          |
|     |         | 1: Stop incrementing the mhpmcounter9 counter.                              |
|     | (R/W)   |                                                                             |
| 10  | HPM8    | Configures the incrementing of mhpmcounter8.                                |
|     |         | 0: Continue incrementing the mhpmcounter8 counter.                          |
|     |         | 1: Stop incrementing the mhpmcounter8 counter.                              |
|     | (R/W)   |                                                                             |
| 7   | IR      | Configures the incrementing of the instret counter.                          |
|     |         | 0: Continue incrementing the instret counter.                               |
|     |         | 1: Stop incrementing the instret counter.                                  |
|     | (R/W)   |                                                                             |
| 6   | TM      | Configures the incrementing of the time counter.                             |
|     |         | 0: Continue incrementing the time counter.                                 |
|     |         | 1: Stop incrementing the time counter.                                     |
|     | (R/W)   |                                                                             |
| 5   | CY      | Configures the incrementing of the cycle counter.                            |
|     |         | 0: Continue incrementing the cycle counter.                                |
|     |         | 1: Stop incrementing the cycle counter.                                    |
|     | (R/W)   |                                                                             |

Register 1.34. mhpmvent8 (0x328)

| Bit | Field           | Description                                                                 |
|-----|-----------------|-----------------------------------------------------------------------------|
| 31  |                 | (reserved)                                                                  |
| 5   | EVENT[4:0]      | Event selector for mhpmcounter8.                                            |
|     |                 | The only valid event value for this counter is 0x6, for conditional branch mispredictions. |
|     | (R/W)           |                                                                             |

```
```markdown
Espressif Systems
59
ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback PRELIMINARY
```