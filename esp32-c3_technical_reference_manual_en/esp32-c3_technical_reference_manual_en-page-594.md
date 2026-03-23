
```markdown
Register 26.37. UHCI_HUNG_CONF_REG (0x0024)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| 0   | 0   | 0   | 0   | 0   | 0   | 0   | 1   | 0   |     | Ox10|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     | Reset |

UHCI_TXFIFO_TIMEOUT    This field stores the timeout value. UHCI will produce the UHCI_TX_HUNG_INT interrupt when DMA takes more time to receive data. (R/W)

UHCI_TXFIFO_TIMEOUT_SHIFT  This field is used to configure the maximum tick count. (R/W)

UHCI_TXFIFO_TIMEOUT_ENA   This is the enable bit for TX FIFO receive timeout. (R/W)

UHCI_RXFIFO_TIMEOUT    This field stores the timeout value. UHCI will produce the UHCI_RX_HUNG_INT interrupt when DMA takes more time to read data from RAM. (R/W)

UHCI_RXFIFO_TIMEOUT_SHIFT  This field is used to configure the maximum tick count. (R/W)

UHCI_RXFIFO_TIMEOUT_ENA   This is the enable bit for DMA send timeout. (R/W)


Register 26.38. UHCI_ACK_NUM_REG (0x002B)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 1   | Ox0| Reset |

UHCI_ACK_NUM    This is the ACK number used in software flow control. (R/W)

UHCI_ACK_NUM_LOAD  Set this bit to 1, and the value configured by UHCI_ACK_NUM would be loaded. (WT)
```