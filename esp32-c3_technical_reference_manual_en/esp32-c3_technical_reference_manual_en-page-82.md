

```markdown
Register 2.13. GDMA_OUT_PUSH_CHn_REG (n: 0-2) (0x00DC+192*n)

GDMA_OUTFIFO_WDATA_CHn This register stores the data that need to be pushed into GDMA FIFO.
(R/W)

GDMA_OUTFIFO_PUSH_CHn Set this bit to push data into GDMA FIFO. (R/W/SC)


Register 2.14. GDMA_OUT_LINK_CHn_REG (n: 0-2) (0x00E0+192*n)

GDMA_OUTLINK_ADDR_CHn This register stores the 20 least significant bits of the first transmit descriptor's address. (R/W)

GDMA_OUTLINK_STOP_CHn Set this bit to stop GDMA's transmit channel from transferring data.
(R/W/SC)

GDMA_OUTLINK_START_CHn Set this bit to enable GDMA's transmit channel for data transfer.
(R/W/SC)

GDMA_OUTLINK_RESTART_CHn Set this bit to restart a new outlink from the last address. (R/W/SC)

GDMA_OUTLINK_PARK_CHn 1: the transmit descriptor's FSM is in idle state; 0: the transmit descriptor's FSM is working. (RO)
```