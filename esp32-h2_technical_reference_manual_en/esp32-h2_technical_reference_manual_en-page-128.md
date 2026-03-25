

```markdown
Chapter 3 GDMA Controller (GDMA)

Register 3.14. GDMA_IN_LINK_CHn_REG (n: 0-2) (0x0080+0xC0*n)
```

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| 30  | GDMA_INLINK_PARK_CHn |
| 29  | GDMA_INLINK_RESTART_START_CHn |
| 28  | GDMA_INLINK_STOP_CHn |
| 27  | GDMA_INLINK_AUTO_RET_CHn |
| 26  | (reserved)  |
| 25  | (reserved)  |
| 24  | (reserved)  |
| 23  | (reserved)  |
| 22  | (reserved)  |
| 21  | (reserved)  |
| 20  | (reserved)  |
| 19  | GDMA_INLINK_ADDR_CHn |

Reset: `0x000`

GDMA_INLINK_ADDR_CHn Represents the lower 20 bits of the first receive descriptor’s address.  
(R/W)

GDMA_INLINK_AUTO_RET_CHn Configures whether or not to return to the current receive descriptor’s address when there are some errors in current receiving data.  
O: Not return  
1: Return  
(R/W)

GDMA_INLINK_STOP_CHn Configures whether to stop GDMA’s RX channel n from receiving data.  
O: Invalid. No effect  
1: Stop  
(WT)

GDMA_INLINK_START_CHn Configures whether or not to enable GDMA’s RX channel n for data transfer.  
O: Disable  
1: Enable  
(WT)

GDMA_INLINK_RESTART_CHn Configures whether or not to restart RX channel n for GDMA transfer.  
O: Invalid. No effect  
1: Restart  
(WT)

GDMA_INLINK_PARK_CHn Represents the status of the receive descriptor’s FSM.  
O: Running  
1: Idle  
(RO)
```