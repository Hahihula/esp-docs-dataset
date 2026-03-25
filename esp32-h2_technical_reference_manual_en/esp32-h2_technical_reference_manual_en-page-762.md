

```markdown
Register 28.65. UHCI_INT_ENA_REG (0x0000C)
```

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 9   | UHCI_APP_CTRL1_INT_ENA        | Write 1 to enable UHCI_APP_CTRL1_INT. (R/W)                                 |
| 8   | UHCI_OUTLINK_EOF_ERR_INT_ENA  | Write 1 to enable UHCI_OUTLINK_EOF_ERR_INT. (R/W)                           |
| 7   | UHCI_SEND_A_REG_Q_INT_ENA     | Write 1 to enable UHCI_SEND_A_REG_Q_INT. (R/W)                              |
| 6   | UHCI_SEND_S_REG_Q_INT_ENA     | Write 1 to enable UHCI_SEND_S_REG_Q_INT. (R/W)                              |
| 5   | UHCI_TX_HUNG_INT_ENA          | Write 1 to enable UHCI_TX_HUNG_INT. (R/W)                                   |
| 4   | UHCI_RX_HUNG_INT_ENA          | Write 1 to enable UHCI_RX_HUNG_INT. (R/W)                                   |
| 3   | UHCI_TX_START_INT_ENA         | Write 1 to enable UHCI_TX_START_INT. (R/W)                                  |
| 2   | UHCI_RX_START_INT_ENA         | Write 1 to enable UHCI_RX_START_INT. (R/W)                                  |
| 1   |                                | Reset                                                                       |
```