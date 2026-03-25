

```markdown
## 30.9.2 SLC Registers

Register 30.7. SDIO_SLCCONFO_REG (0x0000)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 1  | 1  | 1  | 1  | 0x3| 1  | 1  | 0  | 1  | 1  | 0x3| 0  | 0  | 1  | 1  | 1  | 1  | Ox3| 1  | 1  | 0  | 0  | 0x0| 0  | Reset|

SDIO_SLCO_TX_RST Configures whether to reset TX (host to slave) FSM (finite state machine) in SCLO.
O: No effect
1: Reset
(R/W)

SDIO_SLCO_RX_RST Configures whether to reset RX (slave to host) FSM in SCLO.
O: No effect
1: Reset
(R/W)

SDIO_SLCO_TX_LOOP_TEST Configures whether SCLO loops around when the slave buffer finishes receiving packets from the host.
O: Not loop around
1: Loop around, and hardware will not change the owner bit in the linked list
(R/W)

SDIO_SLCO_RX_LOOP_TEST Configures whether SCLO loops around when the slave buffer finishes sending packets to the host.
O: Not loop around
1: Loop around, and hardware will not change the owner bit in the linked list
(R/W)

SDIO_SLCO_RX_AUTO_WRBACK Configures whether SCLO changes the owner bit of RX linked list.
O: Not change
1: Change
(R/W)

SDIO_SLCO_RX_NO_RESTART_CLR Please initialize to 1, and do not modify it. (R/W)

SDIO_SLCO_RXDSCR_BURST_EN Configures whether SCLO can use AHB burst operation when reading the RX linked list from memory.
O: Only use single operation
1: Can use burst operation
(R/W)
```