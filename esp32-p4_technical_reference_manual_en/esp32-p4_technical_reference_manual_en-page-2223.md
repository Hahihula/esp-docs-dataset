

```markdown
- If `SPI_DATA_DTR_EN` is set, the input data in state DIN or output data in state DOUT will be sent in DTR mode; otherwise the data will be in STR mode.

The control bits `SPI_CMD_DTR_EN`, `SPI_ADDR_DTR_EN`, and `SPI_DATA_DTR_EN` can be configured independently, which means CMD in STR mode, ADDR and DOUT or DIN in DTR mode are supported.

GP-SPI2 can only output SPI2DQS signal, but can not receive the signal. Therefore, only flash or external RAM working in fixed dummy mode (dummy cycles in a read sequence is fixed) are supported.

## Configuration (Take GP-SPI2 as an example)

The register configuration can be as follows:

1. Configure the IO path via HP IO MUX or HP GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure AHB clock (`AHB_CLK`) and module clock (`clk_spi_mst`) for the GP-SPI2 module.
3. Clear `SPI_DOUTDIN` and `SPI_SLAVE_MODE`, to enable master half-duplex communication.
4. Configure GP-SPI2 registers listed in Table 43.5-10.
5. Configure SPI CS setup time and hold time according to Section 43.6.
6. Set the property of SPI2CLK according to Section 43.7.
7. Prepare data according to the selected transfer type:

    - In CPU-controlled MOSI transfer, prepare data in registers `SPI_W0_REG`~`SPI_W15_REG`.
    - In DMA-controlled transfer,

        - configure `SPI_DMA_TX_ENA/SPI_DMA_RX_ENA`,
        - configure DMA TX/RX link,
        - and start DMA TX/RX engine, as described in Section 43.5.7 and Section 43.5.8.

8. Configure interrupts and wait for SPI slave to get ready for transfer.
9. Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` to reset these buffers.
10. Set `SPI_USR` in register `SPI_CMD_REG` to start the transfer and wait for the configured interrupts.

## Application Example (Take GP-SPI2 as an example)

The following example shows how GP-SPI2 accesses flash and external RAM in master half-duplex communication.
```