

```markdown
Register 53.2. TWAI_CMD_REG (0x0004)

| Bit | Name                        | Description                                                                 |
|-----|------------------------------|-----------------------------------------------------------------------------|
| 31  |                              | (reserved)                                                                  |
| 5   | TWAI_TX_REQUEST              | Configures whether to drive nodes to start transmission.<br>0: No effect<br>1: Drive nodes to start transmission (WO)<br><br>TWAI_ABORT_TX Configures whether to cancel a pending transmission request.<br>0: No effect<br>1: Cancel a pending transmission request (WO)<br><br>TWAI_RELEASE_BUFFER Configures whether to release the RX buffer.<br>0: No effect<br>1: Release the RX buffer (WO)<br><br>TWAI_CLEAR_DATA_OVERRUN Configures whether to clear the data overrun status bit.<br>0: No effect<br>1: Clear the data overrun status bit (WO)<br><br>TWAI_SELF_RX_REQUEST Configures whether to drive nodes to start transmitting messages while also receiving messages on the bus simultaneously.<br>0: No effect<br>1: Drive nodes to start transmitting messages while also receiving messages on the bus (set the value of TWAI_TX_REQUEST to 0, or only transmission is allowed) (WO)<br><br>TWAI_SELF_RX_REQUEST | TWAI_CLEAR_DATA_OVERRUN | TWAI_RELEASE_BUFFER | TWAI_ABORT_TX | TWAI_TX_REQUEST |
```