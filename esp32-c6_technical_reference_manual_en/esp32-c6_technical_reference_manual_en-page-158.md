

```markdown
Register 4.18. GDMA_OUT_LINK_CHn_REG (n: 0-2) (0x00E0+0xC0*n)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 30  | GDMA_OUTLINK_ADDR_CHn        |
| 29  | GDMA_OUTLINK_START_CHn       |
| 28  | GDMA_OUTLINK_RESTART_CHn     |
| 27  | GDMA_OUTLINK_STOP_CHn        |
| 26  | GDMA_OUTLINK_PARK_CHn        |
| 0x000 | Reset                     |

GDMA_OUTLINK_ADDR_CHn Represents the lower 20 bits of the first transmit descriptor's address. (R/W)

GDMA_OUTLINK_STOP_CHn Configures whether to stop GDMA's TX channel n from transmitting data.
O: Invalid. No effect
1: Stop
(WT)

GDMA_OUTLINK_START_CHn Configures whether to enable GDMA's TX channel n for data transfer.
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

Register 4.19. GDMA_DATE_REG (0x0068)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 0   | 0                            |
|     | Reset                        |
|     | 0x2202250                    |

GDMA_DATE Version control register. (R/W)
```