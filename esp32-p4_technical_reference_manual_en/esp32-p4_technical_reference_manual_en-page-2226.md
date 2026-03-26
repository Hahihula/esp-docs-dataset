

```markdown
9. Configure all the needed CONF buffers, TX buffers and RX buffers, respectively for each segment before this DMA-controlled transfer begins.

10. Point AXI_DMA_OUTLINK_ADDR_ChN to the head address of the CONF and TX buffer descriptor linked list, and then set AXI_DMA_OUTLINK_START_ChN to start the TX DMA.

11. Clear the bit SPI_RX_EOF_EN in register SPI_DMA_CONF_REG. Point AXI_DMA_INLINK_ADDR_ChN to the head address of the CONF and RX buffer descriptor linked list, and then set AXI_DMA_INLINK_START_ChN to start the RX DMA.

12. Set SPI_USR_CONF to enable CONF state.

13. Set SPI_DMA_SEG_TRANS_DONE_INT_ENA to enable the SPI_DMA_SEG_TRANS_DONE_INT interrupt. Configure other interrupts if needed according to Section 43.11.

14. Wait for all the slaves to get ready for transfer.

15. Set SPI_DMA_AFIFO_RST, SPI_BUF_AFIFO_RST, and SPI_RX_AFIFO_RST to reset these buffers.

16. Set SPI_USR to start this DMA-controlled transfer.

17. Wait for SPI_DMA_SEG_TRANS_DONE_INT interrupt, which means this transfer has finished and the data has been stored into corresponding memory.
```

Note:
Prepare the data to send for each segment in its PREP state. Shall ensure that:
(SPI_CS_SETUP_TIME + 1) × T_SPI_CLK >= 4 × (TAHB_CLK + Tclk_spi_mst)

Configuration of CONF Buffer and Magic Value

In a configurable segmented transfer, only registers which change from the last transaction (segment) need to be re-configured to new values in CONF state. The configuration of other registers can be skipped (i.e., kept the same) to save time and chip resources.

The first word in DMA CONF bufferi, called SPI_BIT_MAP_WORD, defines whether given GP-SPI2 register is to be updated or not in segment i. The relation of SPI_BIT_MAP_WORD and GP-SPI2 registers to update can be seen in Table 43.5-13 Bitmap (BM) Table. If a bit in the BM table is set to 1, its corresponding register value will be updated in this segment. Otherwise, if some registers should be kept from being changed, the related bits should be set to 0.

Table 43.5-13. BM Table for CONF State

| BM Bit | Register       | BM Bit | Register           |
|--------|----------------|--------|--------------------|
| 0      | SPI_ADDR_REG   | 7      | SPI_MISC_REG       |
| 1      | SPI_CTRL_REG   | 8      | SPI_DIN_MODE_REG   |
| 2      | SPI_CLOCK_REG  | 9      | SPI_DIN_NUM_REG    |
| 3      | SPI_USER_REG   | 10     | SPI_DOUT_MODE_REG  |
| 4      | SPI_USER1_REG  | 11     | SPI_DMA_CONF_REG   |
| 5      | SPI_USER2_REG  | 12     | SPI_DMA_INT_ENA_REG|
| 6      | SPI_MS_DLEN_REG| 13     | SPI_DMA_INT_CLR_REG|
```