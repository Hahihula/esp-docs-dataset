**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Body Text:**
When writing data (DOUT state), SPI_USR_MOSI should be configured instead, while SPI_USR_MISO should be cleared. The output data bit length is the value of SPI_MS_DATA_BITLEN + 1. Output data should be configured in GP-SPI data buffer (SPI_WO_REG ~ SPI_W15_REG) in CPU-controlled mode, or GDMA TX buffer in DMA-controlled mode. The data byte order is incremented from LSB (byte 0) to MSB.

Pay special attention to the command value in SPI_USR_COMMAND_VALUE and address value in SPI_USR_ADDR_VALUE.

The configuration of command value is as follows:

**Table Title:**
Table 30.5-9. Sending Sequence of Command Value

| COMMAND_BITLEN^1 | COMMAND_VALUE^2 | BIT_ORDER^3 | Sending Sequence of Command Value |
|-------------------|------------------|-------------|----------------------------------|
| 0 - 7             | [7:0]            | 1           | COMMAND_VALUE[COMMAND_BITLEN:0] is sent first. |
|                   |                  | 0           | COMMAND_VALUE[7:7 - COMMAND_BITLEN]:0 is sent first. |
| 8 - 15            | [15:0]           | 1           | COMMAND_VALUE[7:0] is sent first, and then COMMAND_VALUE[COMMAND_BITLEN:8] is sent. |
|                   |                  | 0           | COMMAND_VALUE[7:0] is sent first, and then COMMAND_VALUE[15:15 - COMMAND_BITLEN] is sent. |

**Table Footnotes:**
^1 SPI_USR_COMMAND_BITLEN: this field is used to configure the bit length of the command.
^2 SPI_USR_COMMAND_VALUE: command value is written into this field. For which part of this field is used, see the table above.

^3 SPI_WR_BIT_ORDER: 0: LSB first; 1: MSB first.

**Additional Information:**
The configuration of address value is as follows:

**Footer Text:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Reference Number:**
ESP32-S3 TRM (Version 1.7)