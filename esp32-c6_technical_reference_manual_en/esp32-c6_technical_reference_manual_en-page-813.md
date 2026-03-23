

```markdown
Register 27.93. UHCI_ESC_CONF3_REG (0x0078)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----:|----:|----:|----:|----:|---|---|---|
|    |     |     | OxdF | OxDb |   |   | Reset |

UHCI_ESC_SEQ2 Configures the character that needs to be decoded. The default value is 0x13 used as a flow control character. (R/W)

UHCI_ESC_SEQ2_CHAR0 Configures the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_ESC_SEQ2_CHAR1 Configures the second character of SLIP escape sequence. The default value is 0xDF. (R/W)


Register 27.94. UHCI_PKT_THRES_REG (0x007C)

| 31 | 13 | 12 | 0 |
|----:|----:|----:|---|
|    |     |     | Reset |

UHCI_PKT_THRS Configures the maximum value of the packet length.
Measurement unit: byte.
Valid only when UHCI_HEAD_EN is O. (R/W)
```