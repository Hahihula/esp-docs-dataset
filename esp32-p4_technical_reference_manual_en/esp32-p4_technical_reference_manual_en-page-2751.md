

```markdown
Register 54.10. SDHOST_CMD_REG (0x002C)

SDHOST_CMD_INDEX    Configures the Command index send to card. (R/W)

SDHOST_RESPONSE_EXPECT   Configures whether to expect response from card.
O: No response expected from card
1: Response expected from card
(R/W)

SDHOST_RESPONSE_LENGTH   Configures response length from card.
O: Short response expected from card
1: Long response expected from card
(R/W)

SDHOST_CHECK_RESPONSE_CRC   Configures whether to check response CRC.
O: Do not check
1: Check response CRC
(R/W)

SDHOST_DATA_EXPECTED   Configures whether to expect data transfer.
O: No data transfer expected
1: Data transfer expected
(R/W)

SDHOST_READ_WRITE   Configures data transfer direction.
O: Read from card
1: Write to card
(R/W)

SDHOST_TRANSFER_MODE   Configures data transfer mode.
O: Block data transfer command
1: Stream data transfer command
(R/W)

SDHOST_SEND_AUTO_STOP   Configures whether to automatically send stop command.
O: No stop command is sent at the end of data transfer
1: Send stop command at the end of data transfer
(R/W)
```
Continued on the next page...
```