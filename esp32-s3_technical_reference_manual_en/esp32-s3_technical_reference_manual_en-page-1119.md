**Title:**
Chapter 30 SPI Controller (SPI)

**Subtitle:**
30.5.71 GP-SPI Functional Blocks

**Image Description and Caption:**
- **Figure:** Figure 30.5-2, GP-SPI Block Diagram.
- The figure shows a block diagram with various components labeled such as CPU, AHB/APB Bus, RX GDMA TX, SPI_CLK Generator, Prescaler Counter, Master FSM, Interrupt Control, Timing Module (FSPI/SP13), and several control signals like SPI_CLK_out control, SPI_CLK_in Mode Control.

**Body Text:**
Figure 30.5-2 shows main functional blocks in GP-SPI, including:

- **Master FSM:** all the features supported in GP-SPI master mode are controlled by this state machine together with register configuration.
  
- **SPI Buffer:** SPI_WO_REG ~ SPI_W15_REG (see Figure 30.5-1). The data transferred in CPU-controlled mode is prepared in this buffer.

- **Timing Module:** capture data on FSPI/SPI3 bus:
  - spi_mst/slv_din/dout_ctrl: convert the TX/RX data into bytes.
  
- **spi_rx_affio:** store the received data.
  
- **buf_tx_affio:** store the data to send.
  
- **dma_tx_affio:** store the data from GDMA.

- **clk_spi_mst:** this clock is the module clock of GP-SPI and derived from PLL_CLK. It is used in GP-SPI master mode, to generate SPI_CLK signal for data transfer and for slaves.

- **SPI CLK Generator:** generate SPI_CLK by dividing clk_spi_mst. The divider is determined by SPI_CLKCNT_N and SPI_CLKDIV_PRE.
  
- **SPI_CLK_out Mode Control:** output the SPI_CLK signal for data transfer and for slaves.
  
- **SPI_CLK_in Mode Control:** capture the SPI_CLK signal from SPI master when GP-SPI works as a slave.

**Footer:**
Espressif Systems
1119 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Navigation Link:**
GoBack