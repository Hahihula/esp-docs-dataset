

```markdown
Register 27.73. UHCI_HUNG_CONF_REG (0x0024)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                    |                                                                             |
| 24  | UHCI_RXFIFO_TIMEOUT_ENA       | Configures whether or not to enable the data reception timeout for RX FIFO.   |
|     |                                | O: Disable                                                                   |
|     |                                | 1: Enable                                                                    |
|     |                                | (R/W)                                                                        |
| 23  | UHCI_RXFIFO_TIMEOUT_SHIFT     | Configures the upper limit of the timeout counter for RX FIFO.               |
|     |                                | (R/W)                                                                        |
| 22  | UHCI_TXFIFO_TIMEOUT_ENA       | Configures whether or not to enable the DMA data reception timeout for TX FIFO.|
|     |                                | O: Disable                                                                   |
|     |                                | 1: Enable                                                                    |
|     |                                | (R/W)                                                                        |
| 21  | UHCI_TXFIFO_TIMEOUT_SHIFT     | Configures the upper limit of the timeout counter for TX FIFO.               |
|     |                                | (R/W)                                                                        |
| 20  | UHCI_TXFIFO_TIMEOUT           | Configures the timeout value for DMA data reception.                         |
|     | Measurement unit: ms. (R/W)    |                                                                             |
| 19  | UHCI_RXFIFO_TIMEOUT_ENA       | Configures whether or not to enable the DMA data transmission timeout.        |
|     |                                | O: Disable                                                                   |
|     |                                | 1: Enable                                                                    |
|     |                                | (R/W)                                                                        |
| 18  | UHCI_RXFIFO_TIMEOUT_SHIFT     | Configures the upper limit of the timeout counter for RX FIFO.               |
|     |                                | (R/W)                                                                        |
| 17  | UHCI_TXFIFO_TIMEOUT_ENA       | Configures whether or not to enable the DMA data reception timeout for TX FIFO.|
|     |                                | O: Disable                                                                   |
|     |                                | 1: Enable                                                                    |
|     |                                | (R/W)                                                                        |
| 16  | UHCI_TXFIFO_TIMEOUT_SHIFT     | Configures the upper limit of the timeout counter for TX FIFO.               |
|     |                                | (R/W)                                                                        |
| 15  | UHCI_RXFIFO_TIMEOUT_ENA       | Configures whether or not to enable the DMA data transmission timeout.        |
|     |                                | O: Disable                                                                   |
|     |                                | 1: Enable                                                                    |
|     |                                | (R/W)                                                                        |
```