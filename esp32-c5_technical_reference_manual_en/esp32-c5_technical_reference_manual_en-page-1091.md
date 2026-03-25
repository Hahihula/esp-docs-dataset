

```markdown
Register 32.71. UHCI_CONF1_REG (0x0014)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 9   | UHCI_SW_START                                                                |
| 8   | UHCI_WAIT_SW_START                                                           |
| 7   | (reserved)                                                                  |
| 6   | UHCI_TX_ACK_NUM_RE                                                          |
| 5   | UHCI_TX_CHECK_SUM_RE                                                       |
| 4   | UHCI_SAVE_HEAD                                                              |
| 3   | UHCI_CRC_DISABLE                                                            |
| 2   | UHCI_SEQ_CHECK_EN                                                           |
| 1   | UHCI_CHECK_SUM_EN                                                           |
| 0   | Reset                                                                       |

UHCI_CHECK_SUM_EN Configures whether or not to enable header checksum validation when UHCI receives a data packet.
O: Disable
1: Enable
(R/W)

UHCI_CHECK_SEQ_EN Configures whether or not to enable the sequence number check when UHCI receives a data packet.
O: Disable
1: Enable
(R/W)

UHCI_CRC_DISABLE Configures whether or not to enable CRC calculation.
O: Disable
1: Enable
Valid only when the Data Integrity Check Present bit in UHCI packet is 1.
(R/W)

UHCI_SAVE_HEAD Configures whether or not to save the packet header when UHCI receives a data packet.
O: Not save
1: Save
(R/W)

UHCI_TX_CHECK_SUM_RE Configures whether or not to encode the data packet with a checksum.
O: Not use checksum
1: Use checksum
(R/W)

UHCI_TX_ACK_NUM_RE Configures whether or not to encode the data packet with an acknowledgment when a reliable packet is to be transmitted.
O: Not use acknowledgement
1: Use acknowledgement
(R/W)
```