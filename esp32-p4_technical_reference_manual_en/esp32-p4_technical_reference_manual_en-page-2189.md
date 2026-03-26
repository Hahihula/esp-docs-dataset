

```markdown
Register 42.92. UHCI_ESC_CONF3_REG (0x0078)

| Bit | Field Name             | Description                                                                 |
|-----|------------------------|-----------------------------------------------------------------------------|
| 31  |                        | (reserved)                                                                  |
| 24  |                        | (reserved)                                                                  |
| 23  |                        | (reserved)                                                                  |
| 16  | UHCI_ESC_SEQ2_CHAR0    | Configures the first character of SLIP escape sequence. The default value is 0xDB. (R/W) |
| 15  | UHCI_ESC_SEQ2_CHAR1    | Configures the second character of SLIP escape sequence. The default value is 0xDF. (R/W) |
| 8   |                        | (reserved)                                                                  |
| 7   |                        | (reserved)                                                                  |
| 0   | UHCI_ESC_SEQ2          | Configures the character that needs to be decoded. The default value is 0x13 used as a flow control character. (R/W) |

Register 42.93. UHCI_PKT_THRES_REG (0x007C)

| Bit | Field Name             | Description                                                                 |
|-----|------------------------|-----------------------------------------------------------------------------|
| 31  |                        | (reserved)                                                                  |
| 13  |                        | (reserved)                                                                  |
| 12  | UHCI_PKT_THRS          | Configures the maximum value of the packet length. Measurement unit: byte. Valid only when UHCI_HEAD_EN is 0. (R/W) |
```