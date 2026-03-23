

```markdown
Register 4.14. GDMA_IN_LINK_CHn_REG (n: 0-2) (0x0080+0xC0*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | ... | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|-----|---|
|     |    |    |    |    |    |    | (reserved) | GDMA_INLINK_PARK_CHn | GDMA_INLINK_RESTART_CHn | GDMA_INLINK_START_CHn | GDMA_INLINK_STOP_CHn | GDMA_INLINK_AUTO_RET_CHn | ... | 0 |
| Value | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 | Reset |

GDMA_INLINK_ADDR_CHn Represents the lower 20 bits of the first receive descriptor’s address. (R/W)

GDMA_INLINK_AUTO_RET_CHn Configures whether or not to return to the current receive descriptor’s address when there are some errors in current receiving data.
- O: Not return
- 1: Return
(R/W)

GDMA_INLINK_STOP_CHn Configures whether to stop GDMA’s RX channel n from receiving data.
- O: Invalid. No effect
- 1: Stop
(WT)

GDMA_INLINK_START_CHn Configures whether or not to enable GDMA’s RX channel n for data transfer.
- O: Disable
- 1: Enable
(WT)

GDMA_INLINK_RESTART_CHn Configures whether to restart RX channel n for GDMA transfer.
- O: Invalid. No effect
- 1: Restart
(WT)

GDMA_INLINK_PARK_CHn Represents the status of the receive descriptor’s FSM.
- O: Running
- 1: Idle
(RO)
```