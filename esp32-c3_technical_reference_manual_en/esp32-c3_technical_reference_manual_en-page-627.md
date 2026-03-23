

```markdown
Chapter 27 SPI Controller (SPI)
GoBack

Configuration

To start a data transfer, follow the steps below:

* Configure the IO path via IO MUX or GPIO matrix between GP-SPI2 and an external SPI device.
* Configure APB clock (APB_CLK, see Chapter 6 Reset and Clock) and module clock (clk_spi_mst) for the GP-SPI2 module.
* Set `SPI_DOUTDIN` and clear `SPI_SLAVE_MODE`, to enable full-duplex communication in master mode.
* Configure GP-SPI2 registers listed in Table 27.5-7.
* Configure SPI CS setup time and hold time according to Section 27.6.
* Set the property of FSPICLK according to Section 27.7.
* Prepare data according to the selected transfer mode:

    - In CPU-controlled MOSI mode, prepare data in registers `SPI_W0_REG ~ SPI_W15_REG`.
    - In DMA-controlled mode,

        * configure `SPI_DMA_TX_ENA/SPI_DMA_RX_ENA`
        * configure GDMA TX/RX link
        * start GDMA TX/RX engine, as described in Section 27.5.6 and Section 27.5.7.

* Configure interrupts and wait for SPI slave to get ready for transfer.
* Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` to reset these buffers.
* Set `SPI_USR` in register `SPI_CMD_REG` to start the transfer and wait for the configured interrupts.

27.5.8.4 Half-Duplex Communication (1/2/4-bit Mode)

Introduction

In this mode, GP-SPI2 provides CLK and CS signals. Only one side (SPI master or slave) can send data at a time, while the other side receives the data. To enable this communication mode, clear the bit `SPI_DOUTDIN` in register `SPI_USER_REG`. The standard format of SPI half-duplex communication is CMD + [ADDR+] [DUMMY+] [DOUT or DIN]. The states ADDR, DUMMY, DOUT, and DIN are optional, and can be disabled or enabled independently.

As described in Section 27.5.8.2, the properties of GP-SPI2 states: CMD, ADDR, DUMMY, DOUT and DIN, such as cycle length, value, and parallel bus bit mode, can be set independently. For the register configuration, see Table 27.5-7.

The detailed properties of half-duplex GP-SPI2 are as follows:

1. CMD: 0 ~ 16 bits, master output, slave input.
2. ADDR: 0 ~ 32 bits, master output, slave input.
3. DUMMY: 0 ~ 256 FSPICLK cycles, master output, slave input.
4. DOUT: 0 ~ 512 bits (64 B) in CPU-controlled mode and 0 ~ 256 Kbits (32 KB) in DMA-controlled mode, master output, slave input.

Espressif Systems
627
ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback
```