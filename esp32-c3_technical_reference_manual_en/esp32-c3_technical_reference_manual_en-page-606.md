

```markdown
Register 26.62. UHCI_INT_CLR_REG (0x0010)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 9   | UHCI_APP_CTRL1_INT_CLR                                                      |
| 8   | UHCI_APP_CTRL0_INT_CLR                                                      |
| 7   | UHCI_OUTLINK_EOF_ERR_INT_CLR                                               |
| 6   | UHCI_SEND_A_REG_Q_INT_CLR                                                   |
| 5   | UHCI_SEND_S_REG_Q_INT_CLR                                                   |
| 4   | UHCI_TX_HUNG_INT_CLR                                                        |
| 3   | UHCI_RX_HUNG_INT_CLR                                                        |
| 2   | UHCI_TX_START_INT_CLR                                                       |
| 1   | UHCI_TX_START_INT_CLR                                                       |
| 0   | Reset                                                                      |

UHCI_RX_START_INT_CLR Set this bit to clear UHCI_RX_START_INT interrupt. (WT)
UHCI_TX_START_INT_CLR Set this bit to clear UHCI_TX_START_INT interrupt. (WT)
UHCI_RX_HUNG_INT_CLR Set this bit to clear UHCI_RX_HUNG_INT interrupt. (WT)
UHCI_TX_HUNG_INT_CLR Set this bit to clear UHCI_TX_HUNG_INT interrupt. (WT)
UHCI_SEND_S_REG_Q_INT_CLR Set this bit to clear UHCI_SEND_S_REG_Q_INT interrupt. (WT)
UHCI_SEND_A_REG_Q_INT_CLR Set this bit to clear UHCI_SEND_A_REG_Q_INT interrupt. (WT)
UHCI_OUTLINK_EOF_ERR_INT_CLR Set this bit to clear UHCI_OUTLINK_EOF_ERR_INT interrupt. (WT)
UHCI_APP_CTRL0_INT_CLR Set this bit to clear UHCI_APP_CTRL0_INT interrupt. (WT)
UHCI_APP_CTRL1_INT_CLR Set this bit to clear UHCI_APP_CTRL1_INT interrupt. (WT)

Register 26.63. UHCI_STATE0_REG (0x0018)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 6   | UHCI_RX_ERR_CAUSE                                                          |
| 5   | UHCI_DECODER_STATE                                                         |
| 3   | Reset                                                                      |

UHCI_RX_ERR_CAUSE This field indicates the error type when DMA has received a packet with error. 3'b001: Checksum error in the HCI packet; 3'b010: Sequence number error in the HCI packet; 3'b011: CRC bit error in the HCI packet; 3'b100: 0xCO is found but the received the HCI packet is not end; 3'b101: 0xCO is not found when the HCI packet has been received; 3'b110: CRC check error. (RO)

UHCI_DECODER_STATE UHCI decoder status. (RO)
```