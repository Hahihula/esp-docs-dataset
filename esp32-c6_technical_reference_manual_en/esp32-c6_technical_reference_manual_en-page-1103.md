

```markdown
Register 33.24. TWAI_STATUS_REG (0x0008)

| Bit | Name                     | Description                                                                 |
|-----|--------------------------|-----------------------------------------------------------------------------|
| 31  |                          | (reserved)                                                                  |
| 9   | TWAI_MISS_ST             | Represents whether or not the data packet in the RX FIFO is complete.        |
| 8   | TWAI_BUS_OFF_ST          | Represents whether or not the TWAI Controller involves in bus activities in bus-off status. |
| 7   | TWAI_ERR_ST              | Represents at least one of the RX/TX error counter has reached or exceeded the value set in register TWAI_ERR_WARNING_LIMIT_REG. (RO) |
| 6   | TWAI_TX_ST               | Represents whether or not the TWAI Controller is transmitting a message to the bus. O: Not transmitting<br>1: Transmitting (RO) |
| 5   | TWAI_RX_ST               | Represents whether or not the TWAI Controller is receiving a message from the bus. O: Not receiving<br>1: Receiving (RO) |
| 4   | TWAI_TX_COMPLETE         | Represents whether or not the TWAI controller has received a packet from the bus. O: Not received<br>1: Received (RO) |
| 3   | TWAI_TX_BUF_ST           | Represents whether or not the TX buffer is empty. O: Not empty<br>1: Empty, and the CPU may write a message into it (RO) |
| 2   | TWAI_RX_BUF_ST           | Represents whether or not the RX buffer is empty. O: Empty<br>1: Not empty, with at least one received data packet. (RO) |
| 1   | TWAI_OVERRUN_ST          | Represents whether or not the RX FIFO is full. O: Not full<br>1: Full, and data overrun has occurred (RO) |
```