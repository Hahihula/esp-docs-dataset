

```markdown
Register 26.61. UHCI_INT_ENA_REG (0x000C)
```

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 9   | UHCI_APP_CTRL1_INT_ENA         | This is the interrupt enable bit for UHCI_APP_CTRL1_INT interrupt. (R/W)    |
| 8   | UHCI_OUTLINK_EOF_ERR_INT_ENA   | This is the interrupt enable bit for UHCI_OUTLINK_EOF_ERR_INT interrupt. (R/W)|
| 7   | UHCI_SEND_A_REG_Q_INT_ENA      | This is the interrupt enable bit for UHCI_SEND_A_REG_Q_INT interrupt. (R/W) |
| 6   | UHCI_SEND_S_REG_Q_INT_ENA      | This is the interrupt enable bit for UHCI_SEND_S_REG_Q_INT interrupt. (R/W) |
| 5   | UHCI_TX_HUNG_INT_ENA           | This is the interrupt enable bit for UHCI_TX_HUNG_INT interrupt. (R/W)       |
| 4   | UHCI_RX_HUNG_INT_ENA           | This is the interrupt enable bit for UHCI_RX_HUNG_INT interrupt. (R/W)       |
| 3   | UHCI_TX_START_INT_ENA          | This is the interrupt enable bit for UHCI_TX_START_INT interrupt. (R/W)      |
| 2   | UHCI_RX_START_INT_ENA          | This is the interrupt enable bit for UHCI_RX_START_INT interrupt. (R/W)      |
```