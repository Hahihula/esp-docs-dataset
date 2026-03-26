

```markdown
- One byte from master to slave.
- Can be sent in 1-bit, 2-bit or 4-bit modes according to the command.

3. DUMMY:
    - Its value is meaningless. SPI slave prepares data in this state.
    - Bit mode of SPI2 bus is also meaningless here.
    - Last for eight SPI_CLK cycles.

4. DIN or DOUT:
    - Data length can be 0~64 bytes in CPU-controlled transfer and unlimited in DMA-controlled transfer.
    - Can be sent in 1-bit, 2-bit or 4-bit modes according to the CMD value.
```

```markdown
Note:

The states of ADDR and DUMMY can never be skipped in any half-duplex communications.

When a half-duplex transaction is complete, the transferred CMD and ADDR values are latched into SPI_SLV_LAST_COMMAND and SPI_SLV_LAST_ADDR, respectively. SPI_SLV_CMD_ERR_INT_RAW will be set if the transferred CMD value is not supported by GP-SPI as slave. SPI_SLV_CMD_ERR_INT_RAW can only be cleared by software.
```

```markdown
43.5.10.2    CMD Values Supported in Half-Duplex Communication

In half-duplex communication, the defined values of CMD determine the transfer types. Unsupported CMD values are disregarded, meanwhile the related transfer is ignored and SPI_SLV_CMD_ERR_INT_RAW is set. The transfer format is CMD (8 bits) + ADDR (8 bits) + DUMMY (8 SPI_CLK cycles) + DATA (unit in bytes). The detailed description of CMD[3:0] is as follows:

- 0x1 (Wr_BUF): CPU-controlled write operation. Master sends data and GP-SPI receives data. The data is stored in the related address of SPI_WO_REG~SPI_W15_REG.
- 0x2 (Rd_BUF): CPU-controlled read operation. Master receives the data sent by GP-SPI. The data comes from the related address of SPI_WO_REG~SPI_W15_REG.
- 0x3 (Wr_DMA): DMA-controlled write operation. Master sends data and GP-SPI receives data. The data is stored in GP-SPI DMA RX buffer.
- 0x4 (Rd_DMA): DMA-controlled read operation. Master receives the data sent by GP-SPI. The data comes from GP-SPI DMA TX buffer.
- 0x7 (CMD7): used to generate an SPI_SLV_CMD7_INT interrupt. It can also generate a AXI_DMA_IN_SUC_EOF_Chn_INT interrupt in a slave segmented transfer when DMA RX link is used. But it will not end GP-SPI's slave segmented transfer.
- 0x8 (CMD8): only used to generate an SPI_SLV_CMD8_INT interrupt, which will not end GP-SPI's slave segmented transfer.
- 0x9 (CMD9): only used to generate an SPI_SLV_CMD9_INT interrupt, which will not end GP-SPI's slave segmented transfer.
```