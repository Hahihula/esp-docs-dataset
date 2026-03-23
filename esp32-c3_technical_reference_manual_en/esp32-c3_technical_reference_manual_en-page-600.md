

```markdown
## Register 26.54: UHCI_ESC_CONF0_REG (0x006C)

| 31 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |     |     |     |     |     |     |     |     | Oxdc | Oxdb | Oxco | Reset |

UHCI_SEPER_CHAR  This field is used to define separators to encode data packets. The default value is 0xCO. (R/W)

UHCI_SEPER_ESC_CHARO  This field is used to define the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_SEPER_ESC_CHART  This field is used to define the second character of SLIP escape sequence. The default value is 0xDC. (R/W)


## Register 26.55: UHCI_ESC_CONF1_REG (0x0070)

| 31 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |     |     |     |     |     |     |     | Oxdd | Oxdb | Oxdb | Reset |

UHCI_ESC_SEQO  This field is used to define a character that need to be encoded. The default value is 0xDB that used as the first character of SLIP escape sequence. (R/W)

UHCI_ESC_SEQO_CHARO  This field is used to define the first character of SLIP escape sequence. The default value is 0xDB. (R/W)

UHCI_ESC_SEQO_CHAR1  This field is used to define the second character of SLIP escape sequence. The default value is 0xDD. (R/W)
```