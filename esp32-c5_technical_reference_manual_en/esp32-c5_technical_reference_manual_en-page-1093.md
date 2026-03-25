

```markdown
Register 32.72. UHCI_ESCAPE_CONF_REG (0x0020)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | UHCI_RX_13_ESC_EN                                                           |
| 29  | UHCI_RX_11_ESC_EN                                                           |
| 28  | UHCI_RX_DB_ESC_EN                                                           |
| 27  | UHCI_RX_CO_ESC_EN                                                           |
| 26  | UHCI_TX_13_ESC_EN                                                           |
| 25  | UHCI_TX_11_ESC_EN                                                           |
| 24  | UHCI_TX_DB_ESC_EN                                                           |
| 23  | UHCI_TX_CO_ESC_EN                                                           |
| 22-8| (reserved)                                                                  |
| 7   | 0                                                                             |
| 6   | 1                                                                             |
| 5   | 1                                                                             |
| 4   | 1                                                                             |
| 3   | 1                                                                             |
| 2   | 1                                                                             |
| 1   | 1                                                                             |
| 0   | Reset                                                                        |

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