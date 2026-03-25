

```markdown
Register 28.56. UHCI_REG_Q6_WORD0_REG (0x0064)

UHCI_SEND_Q6_WORD0 Data to be transmitted in Q6 register. (R/W)


Register 28.57. UHCI_REG_Q6_WORD1_REG (0x0068)

UHCI_SEND_Q6_WORD1 Data to be transmitted in Q6 register. (R/W)


Register 28.58. UHCI_ESC_CONFQ_REG (0x006C)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----:|:----|:----|:----|:----|:-:|:-:|:-|
|    |     |     | Oxdc| Oxdb|Oxc0|Reset|

UHCI_SEPER_CHAR Configures separators to encode data packets. The default value is 0xC0. (R/W)

UHCI_SEPER_ESC_CHARO Configures the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_SEPER_ESC_CHAR1 Configures the second character of SLIP escape sequence. The default value is 0xDC. (R/W)
```