

```markdown
Register 39.7. SDIO_SLCCONFO_REG (0x0000)

Continued from the previous page...

SDIO_SLCO_RXDATA_BURST_EN Configures whether SCLO can use AHB burst operation when read data from memory.
O: Only use single operation
1: Can use burst operation
(R/W)

SDIO_SLCO_TXDSCR_BURST_EN Configures whether SCLO can use AHB burst operation when read the TX linked list from memory.
O: Only use single operation
1: Can use burst operation
(R/W)

SDIO_SLCO_TXDATA_BURST_EN Configures whether SCLO can use AHB burst operation when send data to memory.
O: Only use single operation
1: Can use burst operation
(R/W)

SDIO_SLCO_TOKEN_AUTO_CLR Please initialize to 0, and do not modify it. (R/W)

SDIO_SLC1_TX_RST Configures whether to reset TX FSM in SLC1.
O: No effect
1: Reset
(R/W)

SDIO_SLC1_RX_RST Configures whether to reset RX FSM in SLC1.
O: No effect
1: Reset
(R/W)

SDIO_SLC1_TX_LOOP_TEST Configures whether SCL1 loops around when the slave buffer finishes receiving packets from the host.
O: Not loop around
1: Loop around, and hardware will not change the owner bit in the linked list
(R/W)

SDIO_SLC1_RX_LOOP_TEST Configures whether SCL1 loops around when the slave buffer finishes sending packets to the host.
O: Not loop around
1: Loop around, and hardware will not change the owner bit in the linked list
(R/W)

Continued on the next page...
```