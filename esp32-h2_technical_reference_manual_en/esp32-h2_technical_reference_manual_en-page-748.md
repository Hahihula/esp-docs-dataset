

```markdown
Register 28.40. UHCI_ESCAPE_CONF_REG (0x0020)

| Bit | Name                     | Description                                                                 |
|-----|--------------------------|-----------------------------------------------------------------------------|
| 31  |                          | (reserved)                                                                  |
| 30  |                          | (reserved)                                                                  |
| 29  |                          | (reserved)                                                                  |
| 28  |                          | (reserved)                                                                  |
| 27  |                          | (reserved)                                                                  |
| 26  |                          | (reserved)                                                                  |
| 25  |                          | (reserved)                                                                  |
| 24  |                          | (reserved)                                                                  |
| 23  |                          | (reserved)                                                                  |
| 22  |                          | (reserved)                                                                  |
| 21  |                          | (reserved)                                                                  |
| 20  |                          | (reserved)                                                                  |
| 19  |                          | (reserved)                                                                  |
| 18  |                          | (reserved)                                                                  |
| 17  |                          | (reserved)                                                                  |
| 16  |                          | (reserved)                                                                  |
| 15  |                          | (reserved)                                                                  |
| 14  |                          | (reserved)                                                                  |
| 13  |                          | (reserved)                                                                  |
| 12  |                          | (reserved)                                                                  |
| 11  |                          | (reserved)                                                                  |
| 10  |                          | (reserved)                                                                  |
| 9   |                          | (reserved)                                                                  |
| 8   |                          | (reserved)                                                                  |
| 7   |                          | (reserved)                                                                  |
| 6   |                          | (reserved)                                                                  |
| 5   |                          | (reserved)                                                                  |
| 4   |                          | (reserved)                                                                  |
| 3   |                          | (reserved)                                                                  |
| 2   |                          | (reserved)                                                                  |
| 1   |                          | (reserved)                                                                  |
| 0   |                          | Reset                                                                       |

UHCI_TX_CO_ESC_EN Configures whether or not to decode character 0xCO when DMA receives data.
O: Not decode
1: Decode
(R/W)

UHCI_TX_DB_ESC_EN Configures whether or not to decode character 0xDB when DMA receives data.
O: Not decode
1: Decode
(R/W)

UHCI_TX_11_ESC_EN Configures whether or not to decode flow control character 0x11 when DMA receives data.
O: Not decode
1: Decode
(R/W)

UHCI_TX_13_ESC_EN Configures whether or not to decode flow control character 0x13 when DMA receives data.
O: Not decode
1: Decode
(R/W)

UHCI_RX_CO_ESC_EN Configures whether or not to replace 0xCO by special characters when DMA sends data.
O: Not replace
1: Replace
(R/W)

UHCI_RX_DB_ESC_EN Configures whether or not to replace 0xDB by special characters when DMA sends data.
O: Not replace
1: Replace
(R/W)
```