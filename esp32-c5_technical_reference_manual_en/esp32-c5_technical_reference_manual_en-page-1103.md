

```markdown
Register 32.91. UHCI_ESC_CONF1_REG (0x0070)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----:|----:|----:|----:|----:|---:|---:|---:|
|    | o   | o   | o   | o   | o | o | Reset |
|    |     |     | Oxdd| Oxdb|    |    |      |

UHCI_ESC_SEQO Configures the character that needs to be encoded. The default value is 0xDB used as the first character of SLIP escape sequence. (R/W)

UHCI_ESC_SEQO_CHARO Configures the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_ESC_SEQO_CHAR1 Configures the second character of SLIP escape sequence. The default value is 0xDD. (R/W)


Register 32.92. UHCI_ESC_CONF2_REG (0x0074)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----:|----:|----:|----:|----:|---:|---:|---:|
|    | o   | o   | o   | o   | o | o | Reset |
|    |     |     | Oxde| Oxdb|    | Ox11|      |

UHCI_ESC_SEQ1 Configures a character that need to be encoded. The default value is 0x11 used as a flow control character. (R/W)

UHCI_ESC_SEQ1_CHARO Configures the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_ESC_SEQ1_CHAR1 Configures the second character of SLIP escape sequence. The default value is 0xDE. (R/W)
```