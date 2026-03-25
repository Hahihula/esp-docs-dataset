

```markdown
Register 38.44. TWAIFD_TX_COMMAND_TXTB_INFO_REG (0x0074)

Continued from the previous page...

TWAIFD_TXB5 Configures whether to issue the command to TX buffer 5. If the number of TX buffers is less than 5, this field is reserved and has no function.
O: Not issue
1: Issue
(WO)

TWAIFD_TXB6 Configures whether to issue the command TX buffer 6. If the number of TX buffers is less than 6, this field is reserved and has no function.
O: Not issue
1: Issue
(WO)

TWAIFD_TXB7 Configures whether to issue the command to TX buffer 7. If the number of TX buffers is less than 7, this field is reserved and has no function.
O: Not issue
1: Issue
(WO)

TWAIFD_TXB8 Configures whether to issue the command to TX buffer 8. If the number of TX buffers is less than 8, this field is reserved and has no function.
O: Not issue
1: Issue
(WO)

TWAIFD_TXT_BUFFER_COUNT Represents the number of TX buffers present in CAN FD. The lowest buffer is always 1. The highest buffer is at index equal to number of present buffers. (RO)
```