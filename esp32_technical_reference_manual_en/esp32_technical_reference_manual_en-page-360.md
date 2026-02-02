**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Section Heading and Subheading with Content:**

- **Subsection:** 
  - "mode2 means when CPOL=1, CPHA=0. When SPI is idle, the clock output is logic high; data changes on the rising edge of the SPI clock and is sampled on the falling edge;"
  
- **Subsection:** 
  - "mode3 means when CPOL=1, CPHA=1. When SPI is idle, the clock output is logic high; data changes on the falling edge of the SPI clock and is sampled on the rising edge."

**Section Title:**
20.4.2 GP-SPI Timing

**Body Text with Code Blocks (formatted as code blocks):**

The data signals of ESP32 GP-SPIC can be mapped to physical pins either via IO_MUX or via IO_MUX and GPIO matrix. Input signals will be delayed by two `clk_app` clock cycles when they pass through the matrix. Output signals will not be delayed.

When GP-SPI is used as master and the data signals are not received by the SPI controller via GPIO matrix, if GP-SPI output clock frequency is `clk_app/2`, register `SPI_MISO_DELAY_MODE` should be set to 0 when configuring the clock polarity. If GP-SPI output clock frequency is not higher than `clk_app/4`, register `SPI_MISO_DELAY_MODE` can be set to the corresponding value in Table **20.4-1** when configuring the clock polarity.

When GP-SPI is used in master mode and the data signals enter the SPI controller via the GPIO matrix:

1. If GP-SPI output clock frequency is `clk_app/2`, register `SPI_MISO_DELAY_MODE` should be set to 0 and the dummy phase should be enabled (SPI_USR_DUMMY = 1) for one `clk_spi` clock cycle (`SPI_USR_DUMMY_CYC`)
   - LELEN = 0 when configuring the clock polarity;
   
2. If GP-SPI output clock frequency is `clk_app/4`, register `SPI_MISO_DELAY_MODE` should be set to 0 when configuring the clock polarity;

3. If GP-SPI output clock frequency is not higher than `clk_app/8`, register `SPI-MISO_DELAY_MODE` can be set to the corresponding value in Table **20.4-1** when configuring the clock polarity.

When GP-SPI is used in slave mode, the clock signal and the data signals should be routed to the SPI controller via the same path; i.e., neither the clock signal nor the data signals passes through GPIO matrix, or both of them pass through GPIO matrix. This is important in ensuring that the signals are not delayed by different time periods before they reach the SPI hardware.

Assume that `t_spi`, `t_pre` and `tv` in Figure **20.4-1** denote SPI clock period, how far ahead data output is, and data output delay time respectively. Assume the SPI slave’s main clock period is `t_spi`. For non-DMA mode0, SPI slave data output is delayed by `tv`:

- `tv < 3.5 * t_app`, if CLK does not pass through GPIO matrix;
  
- `tv < 5.5 * t_app`, if CLK passes through GPIO matrix.

In DMA mode1 and mode3, SPI slave data output is delayed by the same period of time as in non-DMA mode. However, for mode0 and mode2, SPI slave data is output earlier by `t_pre`:

- `t_pre < (t_spi/2 - 5.5 * t_app)`, if CLK does not pass through GPIO matrix;
  
- `t_pre < (t_spi/2 - 7.5 * t_app)`, if CLK passes through GPIO matrix.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback