**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**GoBack Link:** [GoBack](#)

**Body Text:**

data is configured in `SPI_MS_DATA_BITLEN`. The actual bit length used in communication equals to `(SPI_MS_DATA_BITLEN + 1)`.

**Configuration Section - Subtitle: Configuration (Take GP-SPI2 as an example)**

To start a data transfer, follow the steps below:

- Configure the IO path via IOMUX or GPIO matrix between GP-SPI2 and an external SPI device.
- Configure APB clock (APB_CLK, see Chapter 7 Reset and Clock) and module clock (clk_spi_mst) for the GP-SPI2 module.

**List:**
1. Set `SPI_DOUTDIN` and clear `SPI_SLAVE_MODE`, to enable full-duplex communication in master mode.
2. Configure GP-SPI2 registers listed in Table 30.5-8.
3. Configure SPI CS setup time and hold time according to Section 30.6.

**List:**
4. Set the property of FSPICLK according to Section 30.7
   - Prepare data according to the selected transfer mode:
     - In CPU-controlled MSI mode, prepare data in registers `SPI_WO_REG ~ SPI_W15_REG`.
     - In DMA-controlled mode,
       * configure `SPI_DMA_TX_ENA/SPI_DMA_RX_ENA`
       * configure GDMA TX/RX link
       * start GDMA TX/RX engine, as described in Section 30.5.6 and Section 30.5.7.

**List:**
5. Configure interrupts and wait for SPI slave to get ready for transfer.
   - Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` to reset these buffers.
   - Set `SPI_USR` in register `SPI_CMD_REG` to start the transfer and wait for the configured interrupts.

**Subsection Title: 30.5.8.4 Half-Duplex Communication (1/2/4/8-bit Mode)**

**Introduction Section**

In this mode, GP-SPI provides CLK and CS signals. Only one side (SPI master or slave) can send data at a time, while the other side receives the data. To enable this communication mode, clear the bit `SPI_DOUTDIN` in register `SPI_USER_REG`. The standard format of SPI half-duplex communication is CMD + [ADDR + ][DUMMY +] [DOUT or DIN]. The states ADDR, DUMMY, DOUT, and DIN are optional, and can be disabled or enabled independently.

As described in Section 30.5.8.2, the properties of GP-SPI states: CMD, ADDR, DUMMY, DOUT and DIN, such as cycle length, value, and parallel bus bit mode, can be set independently. For the register configuration, see Table 30.5-8.

**Table Description - The detailed properties of half-duplex GP-SPI are as follows:**

1. CMD: 0 ~ 16 bits, master output, slave input.
2. ADDR: 0 ~ 32 bits, master output, slave input.
3. DUMMY: 0 ~ 256 FSPICLK/`SPI3_CLK` cycles, master output, slave input.

**Footer Information:** 
Espressif Systems
Page Number: 1129
Document Title: ESP32-S3 TRM (Version 1.7)
Link to Submit Documentation Feedback