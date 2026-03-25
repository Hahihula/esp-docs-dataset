

```markdown
Register 28.61. UHCI_ESC_CONF3_REG (0x0078)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 24  | UHCI_ESC_SEQ2_CHAR0                                                         |
| 16  | UHCI_ESC_SEQ2_CHAR1                                                         |
| 8   |                                                                             |
| 7   |                                                                             |
| 0   | Reset                                                                       |

UHCI_ESC_SEQ2 Configures the character that needs to be decoded. The default value is 0x13 used as a flow control character. (R/W)

UHCI_ESC_SEQ2_CHAR0 Configures the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_ESC_SEQ2_CHAR1 Configures the second character of SLIP escape sequence. The default value is 0xDF. (R/W)


Register 28.62. UHCI_PKT_THRES_REG (0x007C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 13  |                                                                             |
| 0   | Reset                                                                       |

UHCI_PKT_THRS Configures the maximum value of the packet length.
Measurement unit: byte. Valid only when UHCI_HEAD_EN is 0. (R/W)
```