

```markdown
Note:
When SPI_CLK_MODE is configured to 1 or 2, the bit SPI_CS_HOLD must be set and the value of SPI_CS_HOLD_TIME should be larger than 1.
```

## 43.7.5 Clock Control as Slave

GP-SPI as slave also supports clock modes 0~3. The polarity and phase are configured by the bits `SPI_TSCK_I_EDGE` and `SPI_RSCK_I_EDGE` in register `SPI_USER_REG`. The output edge of data is controlled by `SPI_CLK_MODE_13` in register `SPI_SLAVE_REG`. The detailed register configuration is shown in Table 43.7-2:

Table 43.7-2. Clock Phase and Polarity Configuration as Slave

| Control Bit | Mode 0 | Mode 1 | Mode 2 | Mode 3 |
|-------------|--------|--------|--------|--------|
| SPI_TSCK_I_EDGE | 0      | 1      | 1      | 0      |
| SPI_RSCK_I_EDGE | 0      | 1      | 1      | 0      |
| SPI_CLK_MODE_13 | 0      | 1      | 0      | 1      |

## 43.8 GP-SPI Timing Compensation

### Introduction

The I/O lines are mapped via GPIO matrix or IO MUX. But there is no timing adjustment in IO MUX. The input data and output data can be delayed for 1 or 2 IO MUX operating clock cycles at the rising or falling edge in GPIO matrix. For detailed register configuration, see Chapter 9 GPIO Matrix and IO MUX. Timing compensation is supported only by GP-SPI.

Figure 43.8-1 shows the timing compensation control for GP-SPI as master, including the following paths:

*   "CLK": the output path of GP-SPI bus clock. The clock is sent out by SPI_CLK out control module, passes through GPIO matrix or IO MUX and then goes to an external SPI device.
*   "IN": data input path of GP-SPI (see line 3 path in color purple in Figure 43.8-1). The input data from an external SPI device passes through GPIO matrix or IO MUX, then is adjusted by the Timing Module (see Figure 43.5-2) and finally is stored into spi_rx_afifo.
*   "OUT": data output path of GP-SPI (see line 2 path in color rose-red in Figure 43.8-1). The output data is sent out to the Timing Module, passes through GPIO matrix or IO MUX and is then captured by an external SPI device.
```