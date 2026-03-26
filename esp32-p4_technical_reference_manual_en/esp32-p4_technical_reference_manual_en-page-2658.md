

```markdown
Register 52.22. EMACDEBUG_REG (0x0024)

Continued from the previous page...

MTLRFFLS Represents the status of the fill-level of the RX FIFO.
O: RX FIFO Empty
1: RX FIFO fill level is below the flow-control deactivate threshold
2: RX FIFO fill level is above the flow-control activate threshold
3: RX FIFO Full
(RO)

MTLFRFCS Represents the state of the RX FIFO read Controller.
O: IDLE state
1: Reading frame data
2: Reserved
3: Flushing the frame data and status
(RO)

MTLRFWCAS Represents the state of the MTL RX FIFO Write Controller.
O: Inactive
1: Active and is transferring a received frame to the FIFO.
(RO)

MACRFFCS Represents the state of the small FIFO Read (bit 1) and Write (bit 0) controllers of the MAC Receive Frame Controller Module.
O: Inactive
1: Active
(RO)

MACRPES Represents the state of the MAC GMII or MII receive protocol engine.
O: IDLE
1: Actively receiving data
(RO)
```