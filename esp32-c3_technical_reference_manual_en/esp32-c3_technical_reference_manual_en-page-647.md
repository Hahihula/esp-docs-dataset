

```markdown
5. Or wait for SPI_SLV_RD_DMA_DONE_INT.
6. Or wait for SPI_SLV_RD_BUF_DONE_INT.
7. Slave should set the total read data byte length in SPI_MS_DATA_BITLEN before the transfer begins. And set SPI_RX_EOF_EN 0→1 before the end of the interrupt program.
8. Master and slave should define a method to end the segmented transfer, such as via GPIO interrupt and so on.
9. Master sends End_SEG_TRAN to end the segmented transfer or slave sets the total read data byte length in SPI_MS_DATA_BITLEN and waits for GDMA_IN_SUC_EOF_CHn_INT.
10. Half-duplex Wr_BUF single transfer can be used in a DMA-controlled segmented transfer.
11. Master sends End_SEG_TRAN to end the segmented transfer.
12. Half-duplex Rd_BUF single transfer can be used in a DMA-controlled segmented transfer.

## 27.10 Register Summary

The addresses in this section are relative to SPI base address provided in Table 3.3-3 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **User-defined control registers** | | | |
| SPI_CMD_REG | Command control register | 0x0000 | varies |
| SPI_ADDR_REG | Address value register | 0x0004 | R/W |
| SPI_USER_REG | SPI USER control register | 0x0010 | varies |
| SPI_USER1_REG | SPI USER control register 1 | 0x0014 | R/W |
| SPI_USER2_REG | SPI USER control register 2 | 0x0018 | R/W |
| **Control and configuration registers** | | | |
| SPI_CTRL_REG | SPI control register | 0x0008 | R/W |
| SPI_MS_DLEN_REG | SPI data bit length control register | 0x001C | R/W |
| SPI_MISC_REG | SPI MISC register | 0x0020 | R/W |
| SPI_DMA_CONF_REG | SPI DMA control register | 0x0030 | varies |
| SPI_SLAVE_REG | SPI slave control register | 0x00E0 | varies |
| SPI_SLAVE1_REG | SPI slave control register 1 | 0x00E4 | R/W/SS |
| **Clock control registers** | | | |
| SPI_CLOCK_REG | SPI clock control register | 0x000C | R/W |
| SPI_CLK_GATE_REG | SPI module clock and register clock control | 0x00E8 | R/W |
| **Timing registers** | | | |
| SPI_DIN_MODE_REG | SPI input delay mode configuration | 0x0024 | R/W |
| SPI_DIN_NUM_REG | SPI input delay number configuration | 0x0028 | R/W |
| SPI_DOUT_MODE_REG | SPI output delay mode configuration | 0x002C | R/W |
| **Interrupt registers** | | | |
| SPI_DMA_INT_ENA_REG | SPI DMA interrupt enable register | 0x0034 | R/W |
| SPI_DMA_INT_CLR_REG | SPI DMA interrupt clear register | 0x0038 | WT |
| SPI_DMA_INT_RAW_REG | SPI DMA interrupt raw register | 0x003C | varies |
| SPI_DMA_INT_ST_REG | SPI DMA interrupt status register | 0x0040 | RO |
```