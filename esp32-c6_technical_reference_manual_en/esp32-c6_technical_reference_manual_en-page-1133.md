

```markdown
Register 34.7. SDIO_SLCCONFO_REG (0x0000)

Continued from the previous page...

SDIO_SLC1_RX_AUTO_WRBACK Configures whether SCL1 changes the owner bit of the RX linked list.
O: Not change
1: Change
(R/W)

SDIO_SLC1_RX_NO_RESTART_CLR Please initialize to 1, and do not modify it. (R/W)

SDIO_SLC1_RXDSCR_BURST_EN Configures whether SCL1 can use AHB burst operation when read the RX linked list from memory.
O: Only use single operation
1: Can use burst operation
(R/W)

SDIO_SLC1_RXDATA_BURST_EN Configures whether SCL1 can use AHB burst operation when reading data from memory.
O: Only use single operation
1: Can use burst operation
(R/W)

SDIO_SLC1_TXDSCR_BURST_EN Configures whether SCL1 can use AHB burst operation when read the TX linked list from memory.
O: Only use single operation
1: Can use burst operation
(R/W)

SDIO_SLC1_TXDATA_BURST_EN Configures whether SCL1 can use AHB burst operation when send data to memory.
O: Only use single operation
1: Can use burst operation
(R/W)

SDIO_SLC1_TOKEN_AUTO_CLR Please initialize to 0, and do not modify it. (R/W)
```