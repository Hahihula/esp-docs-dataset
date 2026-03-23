

```markdown
Register 27.74. UHCI_ACK_NUM_REG (0x0028)

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)         |                                                                             |
| 3   | UHCI_ACK_NUM_LOAD  | Configures whether or not load acknowledgements.                            |
|     |                    | 0: Not load                                                                  |
|     |                    | 1: Load                                                                      |
| 2   | UHCI_ACK_NUM       | Configures the number of acknowledgements used in software flow control. (R/W)|
| 1   |                    |                                                                             |
| 0   | Reset              | 0x0                                                                            |

UHCI_ACK_NUM Configures the number of acknowledgements used in software flow control.
(R/W)

UHCI_ACK_NUM_LOAD Configures whether or not load acknowledgements.
0: Not load
1: Load
(WT)
```