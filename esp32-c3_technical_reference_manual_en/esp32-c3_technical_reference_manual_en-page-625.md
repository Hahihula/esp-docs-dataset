

```markdown
Chapter 27 SPI Controller (SPI) GoBack

- Set `SPI_FREAD_QUAD` and `SPI_USR_MISO`.
- Clear `SPI_FREAD_DUAL`.
- Configure GDMA in DMA-controlled mode. In CPU controlled mode, no action is needed.

5. Clear `SPI_USR_MOSI`.

6. Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` to reset these buffers.

7. Set `SPI_USR` to start GP-SPI2 transfer.

When writing data (DOUT state), `SPI_USR_MOSI` should be configured instead, while `SPI_USR_MISO` should be cleared. The output data bit length is the value of `SPI_MS_DATA_BITLEN + 1`. Output data should be configured in GP-SPI2 data buffer (`SPI_W0_REG ~ SPI_W15_REG`) in CPU-controlled mode, or GDMA TX buffer in DMA-controlled mode. The data byte order is incremented from LSB (byte 0) to MSB.

Pay special attention to the command value in `SPI_USR_COMMAND_VALUE` and to address value in `SPI_USR_ ADDR_VALUE`.

The configuration of command value is as follows:

- If `SPI_USR_COMMAND_BITLEN < 8`, the command value is written to `SPI_USR_COMMAND_VALUE[7:0]`. Command value is sent as follows.
    - If `SPI_WR_BIT_ORDER` is set, the lower part of `SPI_USR_COMMAND_VALUE[7:0]`, i.e. `SPI_USR_ COMMAND_VALUE[SPI_USR_COMMAND_BITLEN:0]`, is sent first.
    - If `SPI_WR_BIT_ORDER` is cleared, the higher part of `SPI_USR_COMMAND_VALUE[7:0]`, i.e. `SPI_USR_COM MAND_VALUE[7:7 - SPI_USR_COMMAND_BITLEN]`, is sent first.

- If `7 < SPI_USR_COMMAND_BITLEN < 16`, the command value is written to `SPI_USR_COMMAND_VALUE[15:0]`. Command value is sent as follows.
    - If `SPI_WR_BIT_ORDER` is set, `SPI_USR_COMMAND_VALUE[7:0]` is sent first, and then the lower part of `SPI_USR_COMMAND_VALUE[15:8]`, i.e. `SPI_USR_COMMAND_VALUE[SPI_USR_COMMAND _BITLEN:8]`, is sent.
    - If `SPI_WR_BIT_ORDER` is cleared, `SPI_USR_COMMAND_VALUE[7:0]` is sent first, and then the higher part of `SPI_USR_COMMAND_VALUE[15:8]`, i.e. `SPI_USR_COMMAND_VALUE[15:15 - SPI_USR_COMMAN D_BITLEN]`, is sent.

The configuration of address value is as follows:

- If `SPI_USR_ADDR_BITLEN < 8`, the address value is written to `SPI_USR_ADDR_VALUE[31:24]`. Address value is sent as follows.
    - If `SPI_WR_BIT_ORDER` is set, the lower part of `SPI_USR_ADDR_VALUE[31:24]`, i.e. `SPI_USR_ADD R_VALUE[SPI_USR_ADDR_BITLEN + 24:24]`, is sent first.
    - If `SPI_WR_BIT_ORDER` is cleared, the higher part of `SPI_USR_ADDR_VALUE[31:24]`, i.e. `SPI_USR_ADDR_ VALUE[31:31 - SPI_USR_ADDR_BITLEN]`, is sent first.
```