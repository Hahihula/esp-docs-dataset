

```markdown
| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 9   | UHCI_APP_CTRL1_INT_CLR              | Write 1 to clear UHCI_APP_CTRL1_INT. (WT)                                   |
| 8   | UHCI_APP_CTRL0_INT_CLR              | Write 1 to clear UHCI_APP_CTRL0_INT. (WT)                                   |
| 7   | UHCI_OUTLINK_EOF_ERR_INT_CLR       | Write 1 to clear UHCI_OUTLINK_EOF_ERR_INT. (WT)                            |
| 6   | UHCI_SEND_A_REG_Q_INT_CLR           | Write 1 to clear UHCI_SEND_A_REG_Q_INT. (WT)                                |
| 5   | UHCI_SEND_S_REG_Q_INT_CLR           | Write 1 to clear UHCI_SEND_S_REG_Q_INT. (WT)                                |
| 4   | UHCI_TX_HUNG_INT_CLR                | Write 1 to clear UHCI_TX_HUNG_INT. (WT)                                     |
| 3   | UHCI_RX_HUNG_INT_CLR                | Write 1 to clear UHCI_RX_HUNG_INT. (WT)                                     |
| 2   | UHCI_TX_START_INT_CLR               | Write 1 to clear UHCI_TX_START_INT. (WT)                                    |
| 1   | UHCI_RX_START_INT_CLR               | Write 1 to clear UHCI_RX_START_INT. (WT)                                    |
| 0   | Reset                               |                                                                             |

UHCI_RX_START_INT_CLR    Write 1 to clear UHCI_RX_START_INT. (WT)
UHCI_TX_START_INT_CLR    Write 1 to clear UHCI_TX_START_INT. (WT)
UHCI_RX_HUNG_INT_CLR     Write 1 to clear UHCI_RX_HUNG_INT. (WT)
UHCI_TX_HUNG_INT_CLR     Write 1 to clear UHCI_TX_HUNG_INT. (WT)
UHCI_SEND_S_REG_Q_INT_CLR Write 1 to clear UHCI_SEND_S_REG_Q_INT. (WT)
UHCI_SEND_A_REG_Q_INT_CLR Write 1 to clear UHCI_SEND_A_REG_Q_INT. (WT)
UHCI_OUTLINK_EOF_ERR_INT_CLR Write 1 to clear UHCI_OUTLINK_EOF_ERR_INT. (WT)
UHCI_APP_CTRL0_INT_CLR   Write 1 to clear UHCI_APP_CTRL0_INT. (WT)
UHCI_APP_CTRL1_INT_CLR   Write 1 to clear UHCI_APP_CTRL1_INT. (WT)
```