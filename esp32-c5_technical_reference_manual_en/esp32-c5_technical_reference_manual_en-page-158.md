

```markdown
Register 3.16. TRACE_RESYNC_PROLONGED_REG (0x003C)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 26-24| TRACE_RESYNC_MODE           |
|     |                              |
| 0   | Reset                       |

TRACE_RESYNC_PROLONGED Configures the threshold for the synchronization counter. (R/W)

TRACE_RESYNC_MODE Configures the synchronization mode.
O: Disable the synchronization counter
1: Invalid
2: Synchronization counter counts by packet
3: Synchronization counter counts by cycle
(R/W)

Register 3.17. TRACE_AHB_CONFIG_REG (0x0040)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
|     |                              |
| 6-5 | TRACE_MAX_INCR               |
| 3-2 | TRACE_HBURST                 |
| 0   | Reset                       |

TRACE_HBURST Configures the AHB burst mode.
O: SINGLE
1: INCR (length not defined)
2: INCR4
4: INCR8
Others: Invalid
(R/W)

TRACE_MAX_INCR Configures the maximum burst length for INCR mode. (R/W)
```