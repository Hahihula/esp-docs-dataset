

```markdown
Register 28.42. UHCI_ACK_NUM_REG (0x0028)

| 31 | 30 | 29 | ... | 4 | 3 | 2 | 1 | 0 |
|----:|----:|----:|-----|---:|---:|---:|---:|---:|
|    |    |    |     |   |   |   |   | Ox0 (Reset) |

UHCI_ACK_NUM Configures the number of acknowledgements used in software flow control.
(R/W)

UHCI_ACK_NUM_LOAD Configures whether or not load acknowledgements.
- 0: Not load
- 1: Load
(WT)
```