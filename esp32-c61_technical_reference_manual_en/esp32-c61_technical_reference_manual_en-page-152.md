

```markdown
Register 2.16. TRACE_RESYNC_PROLONGED_REG (0x003C)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 26  | TRACE_RESYNC_MODE   |
| 25  |                     |
| 24  |                     |
| 23  |                     |
|     |                     |
| 0   |                     |

TRACE_RESYNC_PROLONGED Configures the threshold for the synchronization counter. (R/W)

TRACE_RESYNC_MODE Configures the synchronization mode.
- 0: Disable the synchronization counter
- 1: Invalid
- 2: Synchronization counter counts by packet
- 3: Synchronization counter counts by cycle
(R/W)

Register 2.17. TRACE_AHB_CONFIG_REG (0x0040)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
|     |                     |
| 6   | TRACE_MAX_INCR      |
| 5   |                     |
| 3   |                     |
| 2   |                     |
| 0   | TRACE_HBURST        |

TRACE_HBURST Configures the AHB burst mode.
- 0: SINGLE
- 1: INCR (length not defined)
- 2: INCR4
- 4: INCR8
Others: Invalid
(R/W)

TRACE_MAX_INCR Configures the maximum burst length for INCR mode. (R/W)
```