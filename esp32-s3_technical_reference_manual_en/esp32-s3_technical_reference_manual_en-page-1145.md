**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Body Text with Code Block and Note:**

- **Note:** When `SPI_CLK_MODE` is configured to 1 or 2, the bit `SPI_CS_HOLD` must be set and the value of `SPI_CS_HOLD_TIME` should be larger than 1.

**Section Title:**
30.7.3 Clock Control in Slave Mode

**Body Text with Description:**  
GP-SPI slave mode also supports clock modes 0 ~ 3. The polarity and phase are configured by the bits `SPI_TCK`, `_I_EDGE` and `SPI_RSCK_I_EDGE` in register `SPI_USER_REG`. The output edge of data is controlled by `SPI_CLK_`.

- **Mode Control:** MODE_13 in register `SPI_SLAVE_REG`. The detailed register configuration is shown in Table 30.7-2:

**Table Title:**
Table 30.7-2. Clock Phase and Polarity Configuration in Slave Mode

| Control Bit | Mode O   | Mode 1    | Mode 2     | Mode 3 |
|--------------|----------|-----------|------------|--------|
| SPI_TCK_I_EDGE | 0        | 1         | 1          | 0      |
| SPI_RSCK_I_EDGE | 0       | 1         | 1          | 0      |
| SPI_CLK_MODE_13 | 0     | 1         | 0          | 1      |

**Section Title:**
30.8 GP-SPI Timing Compensation

**Introduction (Take GP-SPI2 as an example):**

The I/O lines are mapped via GPIO matrix or IO MUX for GP-SPI2. But there is no timing adjustment in IO MUX.

- The input data and output data can be delayed for 1 or 2 APB_CLK cycles at the rising or falling edge in GPIO matrix.
- For detailed register configuration, see Chapter 6 I0 MUX and GPIO Matrix (GPIO, IO MUX).

**Figure Description:**
Figure 30.8-1 shows the timing compensation control for GP-SPI2 master mode, including the following paths:

- **"CLK":** The output path of GP-SPI2 bus clock. The clock is sent out by SPI_CLK_out control module; passes through GPIO matrix or IO MUX and then goes to an external SPI device.
  
- **"IN":** Data input path of GP-SPI2 (see line 3 in color purple in Figure 30.8-1). The input data from an external SPI device passes through GPIO matrix or IO MUX, then is adjusted by the Timing Module (see Figure 30.5-2) and finally stored into spi_rx_affio.
  
- **"OUT":** Data output path of GP-SPI2 (see line 2 in color rose-red in Figure 30.8-1). The output data is sent out to the Timing Module, passes through GPIO matrix or IO MUX and then captured by an external SPI device.

**Footer:**
Espressif Systems  
Page number: 1145  
Document version: ESP32-S3 TRM (Version 1.7)