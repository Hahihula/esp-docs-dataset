

```markdown
Register 26.36. UHCI_ESCAPE_CONF_REG (0x0020)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |
| 8   |             |
| 7   | UHCI_RX_13_ESC_EN |
| 6   | UHCI_RX_11_ESC_EN |
| 5   | UHCI_RX_DB_ESC_EN |
| 4   | UHCI_RX_CO_ESC_EN |
| 3   | UHCI_TX_13_ESC_EN |
| 2   | UHCI_TX_11_ESC_EN |
| 1   | UHCI_TX_DB_ESC_EN |
| 0   | UHCI_TX_CO_ESC_EN |

UHCI_TX_CO_ESC_EN Set this bit to decode character 0xC0 when DMA receives data. (R/W)
UHCI_TX_DB_ESC_EN Set this bit to decode character 0xDB when DMA receives data. (R/W)
UHCI_TX_11_ESC_EN Set this bit to decode flow control character 0x11 when DMA receives data. (R/W)
UHCI_TX_13_ESC_EN Set this bit to decode flow control character 0x13 when DMA receives data. (R/W)
UHCI_RX_CO_ESC_EN Set this bit to replace 0xC0 by special characters when DMA sends data. (R/W)
UHCI_RX_DB_ESC_EN Set this bit to replace 0xDB by special characters when DMA sends data. (R/W)
UHCI_RX_11_ESC_EN Set this bit to replace flow control character 0x11 by special characters when DMA sends data. (R/W)
UHCI_RX_13_ESC_EN Set this bit to replace flow control character 0x13 by special characters when DMA sends data. (R/W)
```