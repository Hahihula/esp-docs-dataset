

```markdown
Register 26.56. UHCI_ESC_CONF2_REG (0x0074)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----:|----:|----:|----:|----:|----:|----:|----:|
|    | 0   | 0   | Oxde | Oxdb | Ox11 | Reset |

UHCI_ESC_SEQ1 This field is used to define a character that need to be encoded. The default value is 0x11 that used as a flow control character. (R/W)

UHCI_ESC_SEQ1_CHARO This field is used to define the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_ESC_SEQ1_CHAR1 This field is used to define the second character of SLIP escape sequence. The default value is 0xDE. (R/W)


Register 26.57. UHCI_ESC_CONF3_REG (0x0078)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----:|----:|----:|----:|----:|----:|----:|----:|
|    | 0   | 0   | Oxdf | Oxdb | 0x13 | Reset |

UHCI_ESC_SEQ2 This field is used to define a character that need to be decoded. The default value is 0x13 that used as a flow control character. (R/W)

UHCI_ESC_SEQ2_CHARO This field is used to define the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_ESC_SEQ2_CHAR1 This field is used to define the second character of SLIP escape sequence. The default value is 0xDF. (R/W)
```