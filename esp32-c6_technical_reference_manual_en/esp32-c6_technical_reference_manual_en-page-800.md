

```markdown
Register 27.71. UHCI_CONF1_REG (0x0014)
```

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 9   | UHCI_SW_START                  |                                                                             |
| 8   | UHCI_WAIT_SW_START             |                                                                             |
| 7   | (reserved)                    |                                                                             |
| 6   | UHCI_TX_ACK_NUM_RE            | Configures whether or not to encode the data packet with an acknowledgment when a reliable packet is to be transmitted. O: Not use acknowledgment<br>1: Use acknowledgment<br>(R/W) |
| 5   | UHCI_TX_CHECK_SUM_RE          | Configures whether or not to encode the data packet with a checksum.<br>O: Not use checksum<br>1: Use checksum<br>(R/W) |
| 4   | UHCI_SAVE_HEAD                | Configures whether or not to save the packet header when UHCI receives a data packet.<br>O: Not save<br>1: Save<br>(R/W) |
| 3   | UHCI_CRC_DISABLE              | Configures whether or not to enable CRC calculation.<br>O: Disable<br>1: Enable<br>Valid only when the Data Integrity Check Present bit in UHCI packet is 1.<br>(R/W) |
| 2   | UHCI_CHECK_SEQ_EN             | Configures whether or not to enable the sequence number check when UHCI receives a data packet.<br>O: Disable<br>1: Enable<br>(R/W) |
| 1   | UHCI_CHECK_SUM_EN             | Configures whether or not to enable header checksum validation when UHCI receives a data packet.<br>O: Disable<br>1: Enable<br>(R/W) |

Continued on the next page...
```