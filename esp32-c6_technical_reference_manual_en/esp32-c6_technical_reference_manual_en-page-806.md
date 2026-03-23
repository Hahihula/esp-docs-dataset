

```markdown
Register 27.75. UHCI_QUICK_SENT_REG (0x0030)
```

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 8   |                             | Reset                                                                       |
| 7   |                             | UHCI_SINGLE_SEND_EN                                                         |
| 6   |                             | UHCI_ALWAYS_SEND_EN                                                         |
| 4   |                             | UHCI_SINGLE_SEND_NUM                                                       |
| 3   |                             | UHCI_ALWAYS_SEND_NUM                                                       |
| 2   |                             | UHCI_SINGLE_SEND_EN                                                        |
| 1   |                             | UHCI_ALWAYS_SEND_EN                                                        |
| 0   |                             | Reset                                                                       |

**UHCI_SINGLE_SEND_NUM** Configures the source of data to be transmitted in single_send mode.

- 0: Q0 register
- 1: Q1 register
- 2: Q2 register
- 3: Q3 register
- 4: Q4 register
- 5: Q5 register
- 6: Q6 register
- 7: Invalid. No effect (R/W)

**UHCI_SINGLE_SEND_EN** Configures whether or not to enable single_send mode.

- 0: Disable
- 1: Enable (R/W/SC)

**UHCI_ALWAYS_SEND_NUM** Configures the source of data to be transmitted in always_send mode.

- 0: Q0 register
- 1: Q1 register
- 2: Q2 register
- 3: Q3 register
- 4: Q4 register
- 5: Q5 register
- 6: Q6 register
- 7: Invalid. No effect (R/W)

**UHCI_ALWAYS_SEND_EN** Configures whether or not to enable always_send mode.

- 0: Disable
- 1: Enable (R/W)
```