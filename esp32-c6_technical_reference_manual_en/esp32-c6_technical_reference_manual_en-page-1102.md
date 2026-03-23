

```markdown
Register 33.23. TWAI_CMD_REG (0x0004)

TWAI_TX_REQ Configures whether to drive nodes to start transmission.
O: No effect
1: Drive nodes to start transmission
(WO)

TWAI_ABORT_TX Configures whether to cancel a pending transmission request.
O: No effect
1: Cancel a pending transmission request
(WO)

TWAI_RELEASE_BUF Configures whether to release the RX buffer.
O: No effect
1: Release the RX buffer
(WO)

TWAI_CLR_OVERRUN Configures whether to clear the data overrun status bit.
O: No effect
1: Clear the data overrun status bit
(WO)

TWAI_SELF_RX_REQ Configures whether to allow a message be transmitted and received simultaneously.
O: No effect
1: Allow a message to be transmitted and received simultaneously
(WO)
```