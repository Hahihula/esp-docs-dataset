

```markdown
Register 42.90. UHCI_ESC_CONF1_REG (0x0070)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----:|----:|----:|----:|----:|---:|---:|---:|
|    | o   | o   | o   | o   | o | o | Reset |
|    |     |     | Oxdd| Oxdb|    |    |      |

UHCI_ESC_SEQ0 Configures the character that needs to be encoded. The default value is 0xDB used as the first character of SLIP escape sequence. (R/W)

UHCI_ESC_SEQ0_CHAR0 Configures the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_ESC_SEQ0_CHAR1 Configures the second character of SLIP escape sequence. The default value is 0xDD. (R/W)


Register 42.91. UHCI_ESC_CONF2_REG (0x0074)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----:|----:|----:|----:|----:|---:|---:|---:|
|    | o   | o   | o   | o   | o | o | Reset |
|    |     |     | Oxde| Oxdb|    | Ox11|      |

UHCI_ESC_SEQ1 Configures a character that need to be encoded. The default value is 0x11 used as a flow control character. (R/W)

UHCI_ESC_SEQ1_CHAR0 Configures the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_ESC_SEQ1_CHAR1 Configures the second character of SLIP escape sequence. The default value is 0xDE. (R/W)
```