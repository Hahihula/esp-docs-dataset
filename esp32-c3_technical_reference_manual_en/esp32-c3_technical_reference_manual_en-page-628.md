

```markdown
Chapter 27 SPI Controller (SPI)

5. DIN: 0 ~ 512 bits (64 B) in CPU-controlled mode and 0 ~ 256 Kbits (32 KB) in DMA-controlled mode, master input, slave output.

Configuration

The register configuration is as follows:

1. Configure the IO path via IO MUX or GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure APB clock (APB_CLK) and module clock (clk_spi_mst) for the GP-SPI2 module.
3. Clear `SPI_DOUTDIN` and `SPI_SLAVE_MODE`, to enable half-duplex communication in master mode.
4. Configure GP-SPI2 registers listed in Table 27.5-7.
5. Configure SPI CS setup time and hold time according to Section 27.6.
6. Set the property of FSPICLK according to Section 27.7.
7. Prepare data according to the selected transfer mode:

   - In CPU-controlled MOSI mode, prepare data in registers `SPI_W0_REG` ~ `SPI_W15_REG`.
   - In DMA-controlled mode,

     - configure `SPI_DMA_TX_ENA/SPI_DMA_RX_ENA`
     - configure GDMA TX/RX link
     - start GDMA TX/RX engine, as described in Section 27.5.6 and Section 27.5.7.

8. Configure interrupts and wait for SPI slave to get ready for transfer.
9. Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` to reset these buffers.
10. Set `SPI_USR` in register `SPI_CMD_REG` to start the transfer and wait for the configured interrupts.

Application Example

The following example shows how GP-SPI2 to access flash and external RAM in master half-duplex mode.
```