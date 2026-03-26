

```markdown
Register 42.74. UHCI_QUICK_SENT_REG (0x0030)
```

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 30-28|                             | (reserved)                                                                  |
| 27  | UHCI_SINGLE_SEND_NUM        | Configures the source of data to be transmitted in single_send mode.         |
|     |                             | 0: Q0 register                                                               |
|     |                             | 1: Q1 register                                                               |
|     |                             | 2: Q2 register                                                               |
|     |                             | 3: Q3 register                                                               |
|     |                             | 4: Q4 register                                                               |
|     |                             | 5: Q5 register                                                               |
|     |                             | 6: Q6 register                                                               |
|     |                             | 7: Invalid. No effect                                                        |
|     |                             | (R/W)                                                                        |
| 26  | UHCI_SINGLE_SEND_EN         | Configures whether or not to enable single_send mode.                        |
|     |                             | 0: Disable                                                                   |
|     |                             | 1: Enable                                                                     |
|     |                             | (R/W/SC)                                                                      |
| 25-24|                             | (reserved)                                                                  |
| 23  | UHCI_ALWAYS_SEND_NUM        | Configures the source of data to be transmitted in always_send mode.         |
|     |                             | 0: Q0 register                                                               |
|     |                             | 1: Q1 register                                                               |
|     |                             | 2: Q2 register                                                               |
|     |                             | 3: Q3 register                                                               |
|     |                             | 4: Q4 register                                                               |
|     |                             | 5: Q5 register                                                               |
|     |                             | 6: Q6 register                                                               |
|     |                             | 7: Invalid. No effect                                                        |
|     |                             | (R/W)                                                                        |
| 22  | UHCI_ALWAYS_SEND_EN         | Configures whether or not to enable always_send mode.                        |
|     |                             | 0: Disable                                                                   |
|     |                             | 1: Enable                                                                     |
|     |                             | (R/W)                                                                        |

```markdown
Espressif Systems    2182    ESP32-P4 TRM PRELIMINARY
Submit Documentation Feedback
```