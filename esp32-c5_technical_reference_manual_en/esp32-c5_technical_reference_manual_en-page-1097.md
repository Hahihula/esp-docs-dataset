

```markdown
Register 32.75. UHCI_QUICK_SENT_REG (0x0030)
```

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 30  |                             | (reserved)                                                                  |
| 29  |                             | (reserved)                                                                  |
| 28  |                             | (reserved)                                                                  |
| 27  |                             | (reserved)                                                                  |
| 26  |                             | (reserved)                                                                  |
| 25  |                             | (reserved)                                                                  |
| 24  |                             | (reserved)                                                                  |
| 23  |                             | (reserved)                                                                  |
| 22  |                             | (reserved)                                                                  |
| 21  |                             | (reserved)                                                                  |
| 20  |                             | (reserved)                                                                  |
| 19  |                             | (reserved)                                                                  |
| 18  |                             | (reserved)                                                                  |
| 17  |                             | (reserved)                                                                  |
| 16  |                             | (reserved)                                                                  |
| 15  |                             | (reserved)                                                                  |
| 14  |                             | (reserved)                                                                  |
| 13  |                             | (reserved)                                                                  |
| 12  |                             | (reserved)                                                                  |
| 11  |                             | (reserved)                                                                  |
| 10  |                             | (reserved)                                                                  |
| 9   |                             | (reserved)                                                                  |
| 8   |                             | (reserved)                                                                  |
| 7   |                             | (reserved)                                                                  |
| 6   |                             | (reserved)                                                                  |
| 5   |                             | (reserved)                                                                  |
| 4   |                             | (reserved)                                                                  |
| 3   |                             | (reserved)                                                                  |
| 2   |                             | (reserved)                                                                  |
| 1   |                             | (reserved)                                                                  |
| 0   |                             | Reset                                                                       |

UHCI_SINGLE_SEND_NUM Configures the source of data to be transmitted in single_send mode.
- 0: Q0 register
- 1: Q1 register
- 2: Q2 register
- 3: Q3 register
- 4: Q4 register
- 5: Q5 register
- 6: Q6 register
- 7: Invalid. No effect (R/W)

UHCI_SINGLE_SEND_EN Configures whether or not to enable single_send mode.
- 0: Disable
- 1: Enable (R/W/SC)

UHCI_ALWAYS_SEND_NUM Configures the source of data to be transmitted in always_send mode.
- 0: Q0 register
- 1: Q1 register
- 2: Q2 register
- 3: Q3 register
- 4: Q4 register
- 5: Q5 register
- 6: Q6 register
- 7: Invalid. No effect (R/W)

UHCI_ALWAYS_SEND_EN Configures whether or not to enable always_send mode.
- 0: Disable
- 1: Enable (R/W)
```