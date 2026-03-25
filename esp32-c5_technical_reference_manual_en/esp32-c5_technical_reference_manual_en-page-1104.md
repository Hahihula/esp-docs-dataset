

```markdown
Register 32.93. UHCI_ESC_CONF3_REG (0x0078)

| Bit | Field Name             | Description                                                                 |
|-----|------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)            |                                                                             |
| 24  |                        |                                                                             |
| 23  |                        |                                                                             |
| 16  | UHCI_ESC_SEQ2_CHAR0   | Configures the first character of SLIP escape sequence. The default value is 0xDB. (R/W) |
| 15  | UHCI_ESC_SEQ2_CHAR1   | Configures the second character of SLIP escape sequence. The default value is 0xDF. (R/W) |
| 8   |                        |                                                                             |
| 7   |                        |                                                                             |
| 0   | Reset                 |                                                                             |

UHCI_ESC_SEQ2    Configures the character that needs to be decoded. The default value is 0x13 used as a flow control character. (R/W)

UHCI_ESC_SEQ2_CHAR0    Configures the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_ESC_SEQ2_CHAR1    Configures the second character of SLIP escape sequence. The default value is 0xDF. (R/W)


Register 32.94. UHCI_PKT_THRES_REG (0x007C)

| Bit | Field Name             | Description                                                                 |
|-----|------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)            |                                                                             |
| ... |                        |                                                                             |
| 13  |                        |                                                                             |
| 12  | UHCI_PKT_THRS         | Configures the maximum value of the packet length. Measurement unit: byte. Valid only when UHCI_HEAD_EN is 0. (R/W) |
| 0   | Reset                 |                                                                             |

```
```plaintext
(reserved)
UHCI_ESC_SEQ2_CHAR1
UHCI_ESC_SEQ2_CHAR0
UHCI_ESC_SEQ2

(reserved)
UHCI_PKT_THRS
```