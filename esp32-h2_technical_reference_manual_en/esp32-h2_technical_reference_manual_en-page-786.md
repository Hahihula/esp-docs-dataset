

```markdown
- Set `SPI_FREAD_QUAD` and `SPI_USR_MISO`.
- Clear `SPI_FREAD_DUAL`.
- Configure GDMA in DMA-controlled mode. In CPU-controlled mode, no action is needed.

5. Clear `SPI_USR_MOSI`.

6. Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` to reset these buffers.

7. Set `SPI_USR` to start GP-SPI2 transfer.
```

**Note:**

The register configurations in master mode covered in this chapter all require setting the `SPI_UPDATE` bit, which updates the configuration data from the `AHB_CLK` domain to the `clk_spi_mst` clock domain. This operation is not necessary in the slave mode. See above example for specific configuration.

When writing data (DOUT state), `SPI_USR_MOSI` should be configured instead, while `SPI_USR_MISO` should be cleared. The output data bit length is the value of `SPI_MS_DATA_BITLEN + 1`. Output data should be configured in GP-SPI2 data buffer (`SPI_W0_REG ~ SPI_W15_REG`) in CPU-controlled mode, or GDMA TX buffer in DMA-controlled mode. The data byte order is incremented from LSB (byte 0) to MSB.

Pay special attention to the command value in `SPI_USR_COMMAND_VALUE` and to address value in `SPI_USR_ADDR_VALUE`.

The configuration of command value is as follows:

Table 29-5-8. Sending Sequence of Command Value

| COMMAND_BITLEN¹ | COMMAND_VALUE² | BIT_ORDER³ | Sending Sequence of Command Value |
|-----------------|----------------|------------|------------------------------------|
| 0 - 7           | [7:0]          | 1          | `COMMAND_VALUE[COMMAND_BITLEN:0]` is sent first. |
|                 |                | 0          | `COMMAND_VALUE[7:7 - COMMAND_BITLEN]` is sent first. |
| 8 - 15          | [15:0]         | 1          | `COMMAND_VALUE[7:0]` is sent first, and then `COMMAND_VALUE[COMMAND_BITLEN:8]` is sent. |
|                 |                | 0          | `COMMAND_VALUE[7:0]` is sent first, and then `COMMAND_VALUE[15:15 - COMMAND_BITLEN]` is sent. |

¹ `SPI_USR_COMMAND_BITLEN`: this field is used to configure the bit length of the command.
² `SPI_USR_COMMAND_VALUE`: command value is written into this field. For which part of this field is used, see the table above.
³ `SPI_WR_BIT_ORDER`: 0: LSB first; 1: MSB first.

The configuration of address value is as follows:
```