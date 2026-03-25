

```markdown
Register 38.44. TWAIFD_TX_COMMAND_TXTB_INFO_REG (0x0074)

| Bit | Name                     | Description                                                                 |
|-----|--------------------------|-----------------------------------------------------------------------------|
| 31  |                          | (reserved)                                                                  |
| 20  |                          | (reserved)                                                                  |
| 19  |                          | (reserved)                                                                  |
| 16  | TWAIFD_TXTB_BUFFER_COUNT| Number of TX buffers supported.                                             |
| 15  |                          | (reserved)                                                                  |
| 14  | TWAIFD_TXB8              | Configures whether to issue the command to TX buffer 8.                      |
| 13  | TWAIFD_TXB7              | Configures whether to issue the command to TX buffer 7.                      |
| 12  | TWAIFD_TXB6              | Configures whether to issue the command to TX buffer 6.                      |
| 11  | TWAIFD_TXB5              | Configures whether to issue the command to TX buffer 5.                      |
| 10  | TWAIFD_TXB4              | Configures whether to issue the command to TX buffer 4.                      |
| 9   | TWAIFD_TXB3              | Configures whether to issue the command to TX buffer 3. If the number of TX buffers is less than 3, this field is reserved and has no function. |
| 8   | TWAIFD_TXB2              | Configures whether to issue the command to TX buffer 2.                      |
| 7   |                          | (reserved)                                                                  |
| 6   |                          | (reserved)                                                                  |
| 5   |                          | (reserved)                                                                  |
| 4   | O×4                      | Reset value                                                                 |
| 3   | TWAIFD_TXCA              | Configures whether to issue the "set abort" command.                         |
| 2   | TWAIFD_TXCR              | Configures whether to issue the "set ready" command.                         |
| 1   | TWAIFD_TXCE              | Configures whether to issue the "set empty" command.                         |
| 0   |                          | Reset value                                                                 |

TWAIFD_TXCE Configures whether to issue the "set empty" command.
- 0: Not issue
- 1: Issue (WO)

TWAIFD_TXCR Configures whether to issue the "set ready" command.
- 0: Not issue
- 1: Issue (WO)

TWAIFD_TXCA Configures whether to issue the "set abort" command.
- 0: Not issue
- 1: Issue (WO)

TWAIFD_TXB1 Configures whether to issue the command to TX buffer 1.
- 0: Not issue
- 1: Issue (WO)

TWAIFD_TXB2 Configures whether to issue the command to TX buffer 2.
- 0: Not issue
- 1: Issue (WO)

TWAIFD_TXB3 Configures whether to issue the command to TX buffer 3. If the number of TX buffers is less than 3, this field is reserved and has no function.
- 0: Not issue
- 1: Issue (WO)

TWAIFD_TXB4 Configures whether to issue the command to TX buffer 4. If the number of TX buffers is less than 4, this field is reserved and has no function.
- 0: Not issue
- 1: Issue (WO)
```