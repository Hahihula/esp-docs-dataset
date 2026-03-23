

```markdown
Register 2.9. GDMA_IN_POP_CHn_REG (n: 0-2) (0x007C+192*n)

31                                 13   12   11                         0
+--------------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | 0x800 | Reset |
+--------------------------------------------------------------------------------------------------+

GDMA_INFIFO_RDATA_CHn This register stores the data popping from GDMA FIFO (intended for debugging). (RO)

GDMA_INFIFO_POP_CHn Set this bit to pop data from GDMA FIFO (intended for debugging). (R/W/SC)


Register 2.10. GDMA_IN_LINK_CHn_REG (n: 0-2) (0x0080+192*n)

31                                 25   24   23   22   21   20   19                         0
+--------------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 | 1 0 0 0 0 1 | 0x000 | Reset |
+--------------------------------------------------------------------------------------------------+

GDMA_INLINK_ADDR_CHn This register stores the 20 least significant bits of the first receive descriptor's address. (R/W)

GDMA_INLINK_AUTO_RET_CHn Set this bit to return to current receive descriptor's address, when there are some errors in current receiving data. (R/W)

GDMA_INLINK_STOP_CHn Set this bit to stop GDMA's receive channel from receiving data. (R/W/SC)

GDMA_INLINK_START_CHn Set this bit to enable GDMA's receive channel from receiving data. (R/W/SC)

GDMA_INLINK_RESTART_CHn Set this bit to mount a new receive descriptor. (R/W/SC)

GDMA_INLINK_PARK_CHn 1: the receive descriptor's FSM is in idle state; 0: the receive descriptor's FSM is working. (RO)
```