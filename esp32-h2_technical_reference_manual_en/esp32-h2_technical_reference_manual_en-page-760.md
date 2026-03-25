

```markdown
Register 28.63. UHCI_INT_RAW_REG (0x0004)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 9   | UHCI_APP_CTRL1_INT_RAW         | The raw interrupt status of UHCI_APP_CTRL1_INT. (R/W)                        |
| 8   | UHCI_OUTLINK_EOF_ERR_INT_RAW   | The raw interrupt status of UHCI_OUTLINK_EOF_ERR_INT. (R/WTC/SS)             |
| 7   | UHCI_SEND_A_REG_Q_INT_RAW      | The raw interrupt status of UHCI_SEND_A_REG_Q_INT. (R/WTC/SS)                |
| 6   | UHCI_SEND_S_REG_Q_INT_RAW      | The raw interrupt status of UHCI_SEND_S_REG_Q_INT. (R/WTC/SS)                |
| 5   | UHCI_TX_HUNG_INT_RAW            | The raw interrupt status of UHCI_TX_HUNG_INT. (R/WTC/SS)                     |
| 4   | UHCI_RX_HUNG_INT_RAW            | The raw interrupt status of UHCI_RX_HUNG_INT. (R/WTC/SS)                     |
| 3   | UHCI_TX_START_INT_RAW           | The raw interrupt status of UHCI_TX_START_INT. (R/WTC/SS)                    |
| 2   | UHCI_RX_START_INT_RAW           | The raw interrupt status of UHCI_RX_START_INT. (R/WTC/SS)                    |
| 1   |                                 | Reset                                                                        |
```

UHCI_RX_START_INT_RAW  The raw interrupt status of UHCI_RX_START_INT. (R/WTC/SS)

UHCI_TX_START_INT_RAW  The raw interrupt status of UHCI_TX_START_INT. (R/WTC/SS)

UHCI_RX_HUNG_INT_RAW  The raw interrupt status of UHCI_RX_HUNG_INT. (R/WTC/SS)

UHCI_TX_HUNG_INT_RAW  The raw interrupt status of UHCI_TX_HUNG_INT. (R/WTC/SS)

UHCI_SEND_S_REG_Q_INT_RAW  The raw interrupt status of UHCI_SEND_S_REG_Q_INT. (R/WTC/SS)

UHCI_SEND_A_REG_Q_INT_RAW  The raw interrupt status of UHCI_SEND_A_REG_Q_INT. (R/WTC/SS)

UHCI_OUTLINK_EOF_ERR_INT_RAW  The raw interrupt status of UHCI_OUTLINK_EOF_ERR_INT. (R/WTC/SS)

UHCI_APP_CTRL1_INT_RAW  The raw interrupt status of UHCI_APP_CTRL1_INT. (R/W)
```