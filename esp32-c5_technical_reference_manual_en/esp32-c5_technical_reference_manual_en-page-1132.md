

```markdown
Note:

Updating the configuration when the GP-SPI2 works as master described in this and subsequent sections requires setting SPI_UPDATE accordingly to synchronize the configuration from AHB_CLK domain to clk_spi_mst domain. For more detailed configuration, see the sections above. No operation is required when the GP-SPI2 works as slave.

When writing data (DOUT state), SPI_USR_MOSI should be configured instead, while SPI_USR_MISO should be cleared. The output data bit length is the value of SPI_MS_DATA_BITLEN + 1. Output data should be configured in GP-SPI2 data buffer (SPI_WO_REG~SPI_W15_REG) for CPU-controlled transfer, or GDMA TX buffer for DMA-controlled transfer.

Pay special attention to the command value in SPI_USR_COMMAND_VALUE and the address value in SPI_USR_ADDR_VALUE.

The configuration of command value is as follows:

Table 33.5-8. Sending Sequence of Command Value

| COMMAND_BITLEN¹ | COMMAND_VALUE² | BIT_ORDER³ | Sending Sequence of Command Value |
|-----------------|----------------|-----------|-----------------------------------|
| 0~7             | [7:0]          | 1         | COMMAND_VALUE[COMMAND_BITLEN:0] is sent first. <br> O | COMMAND_VALUE[7:7—COMMAND_BITLEN] is sent first. |
| 8~15            | [15:0]         | 1         | COMMAND_VALUE[7:0] is sent first, and then COMMAND_VALUE[COMMAND_BITLEN:8]. <br> O | COMMAND_VALUE[7:0] is sent first, and then COMMAND_VALUE[15:15—COMMAND_BITLEN]. |

¹ SPI_USR_COMMAND_BITLEN: this field is used to configure the bit length of the command.
² SPI_USR_COMMAND_VALUE: command value is written into this field. For which part of this field is used, see the table above.
³ SPI_WR_BIT_ORDER: For the detailed configuration, see Table 33.5-4.

The configuration of address value is as follows:

Table 33.5-9. Sending Sequence of Address Value

| ADDR_BITLEN¹ | ADDR_VALUE² | BIT_ORDER³ | Sending Sequence of Address Value |
|--------------|-------------|-----------|-----------------------------------|
| 0~7          | [31:24]     | 1         | COMMAND_VALUE[ADDR_BITLEN + 24:24] is sent first. <br> O | ADDR_VALUE[31:31—ADDR_BITLEN] is sent first. |
| 8~15         | [31:16]     | 1         | ADDR_VALUE[31:24] is sent first, and then ADDR_VALUE[ADDR_BITLEN + 8:16]. <br> O | ADDR_VALUE[31:24] is sent first, and then ADDR_VALUE[23:31—ADDR_BITLEN]. |
| 16~23        | [31:8]      | 1         | ADDR_VALUE[31:16] is sent first, and then ADDR_VALUE[ADDR_BITLEN—8:8]. |
```