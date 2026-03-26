

```markdown
Register 42.72. UHCI_HUNG_CONF_REG (0x0024)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 24  | UHCI_TXFIFO_TIMEOUT_ENA             | Configures whether or not to enable the data reception timeout for TX FIFO. O: Disable<br>1: Enable<br>(R/W) |
| 23  | UHCI_RXFIFO_TIMEOUT_ENA             | Configures whether or not to enable the DMA data transmission timeout.<br>O: Disable<br>1: Enable<br>(R/W) |
| 22  | UHCI_TXFIFO_TIMEOUT_SHIFT           | Configures the upper limit of the timeout counter for TX FIFO. (R/W)         |
| 20  | UHCI_RXFIFO_TIMEOUT_SHIFT           | Configures the upper limit of the timeout counter for RX FIFO. (R/W)         |
| 19  | UHCI_TXFIFO_TIMEOUT                 | Configures the timeout value for DMA data reception.<br>Measurement unit: ms. (R/W) |
| 12  | UHCI_RXFIFO_TIMEOUT                 | Configures the timeout value for DMA to read data from RAM.<br>Measurement unit: ms. (R/W) |
| 11  | UHCI_TXFIFO_TIMEOUT_ENA             | Configures whether or not to enable the data reception timeout for TX FIFO.<br>O: Disable<br>1: Enable<br>(R/W) |
| 10  | UHCI_RXFIFO_TIMEOUT_ENA             | Configures whether or not to enable the DMA data transmission timeout.<br>O: Disable<br>1: Enable<br>(R/W) |
| 8   | UHCI_TXFIFO_TIMEOUT_SHIFT           |                                                                             |
| 7   | Reset                                |                                                                             |
```