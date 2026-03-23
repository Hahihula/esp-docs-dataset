
```markdown
Register 31.19. TWAI_CMD_REG (0x0004)

TWAI_TX_REQ    Set the bit to 1 to drive nodes to start transmission. (WO)
TWAI_ABORT_TX  Set the bit to 1 to cancel a pending transmission request. (WO)
TWAI_RELEASE_BUF   Set the bit to 1 to release the RX buffer. (WO)
TWAI_CLR_OVERRUN   Set the bit to 1 to clear the data overrun status bit. (WO)
TWAI_SELF_RX_REQ   Self reception request command. Set the bit to 1 to allow a message be transmitted and received simultaneously. (WO)

Register 31.20. TWAI_STATUS_REG (0x0008)

TWAI_RX_BUF_ST    1: The data in the RX buffer is not empty, with at least one received data packet. (RO)
TWAI_OVERRUN_ST   1: The RX FIFO is full and data overrun has occurred. (RO)
TWAI_TX_BUF_ST    1: The TX buffer is empty, the CPU may write a message into it. (RO)
TWAI_TX_COMPLETE  1: The TWAI controller has successfully received a packet from the bus. (RO)
TWAI_RX_ST        1: The TWAI Controller is receiving a message from the bus. (RO)
TWAI_TX_ST        1: The TWAI Controller is transmitting a message to the bus. (RO)
TWAI_ERR_ST       1: At least one of the RX/TX error counter has reached or exceeded the value set in register TWAI_ERR_WARNING_LIMIT_REG. (RO)
TWAI_BUS_OFF_ST   1: In bus-off status, the TWAI Controller is no longer involved in bus activities. (RO)
TWAI_MISS_ST      This bit reflects whether the data packet in the RX FIFO is complete. 1: The current packet is missing; 0: The current packet is complete (RO)
```