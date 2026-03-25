

```markdown
- In master mode, the default compensation scheme delays SPI_CLK by half a cycle. Refer to Figure 33.7-1 and Figure 33.7-2. You can also switch to standard sampling via register configuration.
- If the series register compensation scheme is used, it further improves timing compensation for high-speed transmissions on top of the default half-cycle delay.
- When working as slave, GP-SPI2 follows the standard SPI protocol for data transmission by default. You can also advance data transmission by half a cycle via register configuration.

When GP-SPI2 works as master, it delays the sampling of data returned by the slave by half an SPI clock cycle. You can switch to the standard SPI protocol sampling scheme by setting `SPI_CLK_EDGE_SEL` high. Note that when `SPI_CLK_EQU_SYSCLK` is set to 1, the data sampling from slave is always delayed by half an SPI clock cycle, and at this point, you can use other methods to adjust the IO timing.

The I/O lines are mapped via GPIO matrix or IO MUX. But there is no timing adjustment in IO MUX. The input data and output data can be delayed for 1 or 2 IO MUX operating clock cycles at the rising or falling edge in GPIO matrix. For detailed register configuration, see Chapter 8 GPIO Matrix and IO MUX.

Figure 33.8-1 shows the timing compensation control for GP-SPI2 as master, including the following paths:

*   "CLK": the output path of GP-SPI2 bus clock. The clock is sent out by SPI_CLK out control module, passes through GPIO matrix or IO MUX and then goes to an external SPI device.
*   "IN": data input path of GP-SPI2 (see line 3 path in color purple in Figure 33.8-1). The input data from an external SPI device passes through GPIO matrix or IO MUX, then is adjusted by the Timing Module (see Figure 33.5-2) and finally is stored into spi_rx_afifo.
*   "OUT": data output path of GP-SPI2 (see line 2 path in color rose-red in Figure 33.8-1). The output data is sent out to the Timing Module, passes through GPIO matrix or IO MUX and is then captured by an external SPI device.

Figure 33.8-1. Timing Compensation Control Diagram in GP-SPI as Master
```