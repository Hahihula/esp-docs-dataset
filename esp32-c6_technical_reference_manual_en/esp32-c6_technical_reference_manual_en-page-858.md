

```markdown
The I/O lines are mapped via GPIO Matrix or IO MUX. But there is no timing adjustment in IO MUX. The input data and output data can be delayed for 1 or 2 IO MUX operating clock cycles at the rising or falling edge in GPIO matrix. For detailed register configuration, see Chapter 7 IO MUX and GPIO Matrix (GPIO, IO MUX).

Figure 28.8-1 shows the timing compensation control for GP-SPI2 as master, including the following paths:

*   "CLK": the output path of GP-SPI2 bus clock. The clock is sent out by SPI_CLK out control module, passes through GPIO Matrix or IO MUX and then goes to an external SPI device.
*   "IN": data input path of GPI2. The input data from an external SPI device passes through GPIO Matrix or IO MUX, then is adjusted by the Timing Module and finally is stored into spi_rx_affifo.
*   "OUT": data output path of GP-SPI2. The output data is sent out to the Timing Module, passes through GPIO Matrix or IO MUX and is then captured by an external SPI device.

![Figure 28.8-1. Timing Compensation Control Diagram in GP-SPI2 as Master](image)

Every input and output data is passing through the Timing Module and the module can be used to apply delay in units of Tclk_spi_mst (one cycle of clk_spi_mst) on rising or falling edge.

Key Registers

*   SPI_DIN_MODE_REG: select the latch edge of input data
*   SPI_DIN_NUM_REG: select the delay cycles of input data
*   SPI_DOUT_MODE_REG: select the latch edge of output data

Timing Compensation Example

Figure 28.8-2 shows a timing compensation example in GP-SPI2 as master. Note that DUMMY cycle length is configurable to compensate the delay in I/O lines, so as to enhance the performance of GP-SPI2.
```