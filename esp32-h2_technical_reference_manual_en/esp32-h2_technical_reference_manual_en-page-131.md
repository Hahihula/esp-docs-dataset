

```markdown
Register 3.18. GDMA_OUT_LINK_CHn_REG (n: 0-2) (0x00E0+0xC0*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | GDMA_OUTLINK_ADDR_CHn                                                      |
| 29  | GDMA_OUTLINK_STOP_CHn                                                      |
| 28  | GDMA_OUTLINK_START_CHn                                                     |
| 27  | GDMA_OUTLINK_RESTART_CHn                                                   |
| 26  | GDMA_OUTLINK_PARK_CHn                                                       |
| 25  | (reserved)                                                                  |
| 24  | (reserved)                                                                  |
| 23  | (reserved)                                                                  |
| 22  | (reserved)                                                                  |
| 21  | (reserved)                                                                  |
| 20  | (reserved)                                                                  |
| 19  | (reserved)                                                                  |
| 18  | (reserved)                                                                  |
| 17  | (reserved)                                                                  |
| 16  | (reserved)                                                                  |
| 15  | (reserved)                                                                  |
| 14  | (reserved)                                                                  |
| 13  | (reserved)                                                                  |
| 12  | (reserved)                                                                  |
| 11  | (reserved)                                                                  |
| 10  | (reserved)                                                                  |
| 9   | (reserved)                                                                  |
| 8   | (reserved)                                                                  |
| 7   | (reserved)                                                                  |
| 6   | (reserved)                                                                  |
| 5   | (reserved)                                                                  |
| 4   | (reserved)                                                                  |
| 3   | (reserved)                                                                  |
| 2   | (reserved)                                                                  |
| 1   | (reserved)                                                                  |
| 0   | GDMA_OUTLINK_ADDR_CHn                                                      |

GDMA_OUTLINK_ADDR_CHn Represents the lower 20 bits of the first transmit descriptor's address. (R/W)

GDMA_OUTLINK_STOP_CHn Configures whether to stop GDMA's TX channel n from transmitting data.
O: Invalid. No effect
1: Stop
(WT)

GDMA_OUTLINK_START_CHn Configures whether or not to enable GDMA's TX channel n for data transfer.
O: Disable
1: Enable
(WT)

GDMA_OUTLINK_RESTART_CHn Configures whether to restart TX channel n for GDMA transfer.
O: Invalid. No effect
1: Restart
(WT)

GDMA_OUTLINK_PARK_CHn Represents the status of the transmit descriptor's FSM.
O: Running
1: Idle
(RO)
```

Register 3.19. GDMA_DATE_REG (0x0068)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| ... | ...         |
| 0   | 0           |

GDMA_DATE Version control register. (R/W)
```