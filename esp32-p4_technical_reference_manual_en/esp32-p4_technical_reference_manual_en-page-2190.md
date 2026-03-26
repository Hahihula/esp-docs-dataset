

```markdown
Register 42.94. UHCI_INT_RAW_REG (0x0004)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 30  |                                 | Reset                                                                      |
| 29  | UHCI_RX_START_INT_RAW           | The raw interrupt status of UHCI_RX_START_INT. (R/WTC/SS)                    |
| 28  | UHCI_TX_START_INT_RAW           | The raw interrupt status of UHCI_TX_START_INT. (R/WTC/SS)                    |
| 27  | UHCI_RX_HUNG_INT_RAW            | The raw interrupt status of UHCI_RX_HUNG_INT. (R/WTC/SS)                     |
| 26  | UHCI_TX_HUNG_INT_RAW            | The raw interrupt status of UHCI_TX_HUNG_INT. (R/WTC/SS)                     |
| 25  | UHCI_SEND_S_REG_Q_INT_RAW       | The raw interrupt status of UHCI_SEND_S_REG_Q_INT. (R/WTC/SS)                |
| 24  | UHCI_SEND_A_REG_Q_INT_RAW       | The raw interrupt status of UHCI_SEND_A_REG_Q_INT. (R/WTC/SS)                |
| 23  | UHCI_OUT_EOF_INT_RAW            | The raw interrupt status of UHCI_OUT_EOF_INT. (R/WTC/SS)                     |
| 22  | UHCI_APP_CTRL0_INT_RAW          | The raw interrupt status of UHCI_APP_CTRL0_INT. (R/W)                         |
| 21  | UHCI_APP_CTRL1_INT_RAW          | The raw interrupt status of UHCI_APP_CTRL1_INT. (R/W)                         |
```