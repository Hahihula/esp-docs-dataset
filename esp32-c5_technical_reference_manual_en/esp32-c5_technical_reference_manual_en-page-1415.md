

```markdown
Register 38.18. TWAIFD_STATUS_REG (0x0008)

TWAIFD_RXNE    Represents that the RX buffer is not empty. This field is set to 1 when at least one frame is stored in the RX buffer.
O: Empty
1: Not empty
(RO)

TWAIFD_DOR     Represents the data overrun flag. This field is set when a frame is dropped due to lack of space in the RX buffer. It can be cleared by TWAIFD_RRB.
O: Not overrun
1: Overrun
(RO)

TWAIFD_TXNF    Represents the status of TX buffers. This field is set if at least one TX buffer is empty.
O: Not full
1: Full
(RO)

TWAIFD_EFT     Represents whether an error frame is currently being transmitted.
O: Not being transmitted
1: Being transmitted
(RO)

TWAIFD_RXS     Represents whether CAN FD is the receiver of a CAN frame.
O: Not receiving
1: Receiving
(RO)

TWAIFD_TXS     Represents whether CAN FD is the transmitter of a CAN frame.
O: Not transmitting
1: Transmitting
(RO)

TWAIFD_EWL     Represents whether the TEC or REC reaches (is equal to, or higher than) EWL.
O: Not reach
1: Reach
(RO)

TWAIFD_IDLE    Represents whether the bus is idle (no frame is being transmitted or received) or if CAN FD is in bus-off state. O: Not idle
1: Idle
(RO)
```