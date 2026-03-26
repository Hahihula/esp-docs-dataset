

```markdown
Figure 43.7-2. SPI Clock Mode 1 or 3

1. Mode 0: CPOL = 0, CPHA = 0; SCK is 0 when the SPI is in idle state; data is changed on the falling edge of SCK and sampled on the rising edge. The first data is shifted out before the first falling edge of SCK.
2. Mode 1: CPOL = 0, CPHA = 1; SCK is 0 when the SPI is in idle state; data is changed on the rising edge of SCK and sampled on the falling edge.
3. Mode 2: CPOL = 1, CPHA = 0; SCK is 1 when the SPI is in idle state; data is changed on the rising edge of SCK and sampled on the falling edge. The first data is shifted out before the first rising edge of SCK.
4. Mode 3: CPOL = 1, CPHA = 1; SCK is 1 when the SPI is in idle state; data is changed on the falling edge of SCK and sampled on the rising edge.

43.7.4 Clock Control as Master

The four clock modes 0~3 are supported in GP-SPI as master. The polarity and phase of GP-SPI clock are controlled by the bit SPI_CK_IDLE_EDGE in register SPI_MISC_REG and the bit SPI_CK_OUT_EDGE in register SPI_USER_REG. The register configuration for SPI clock modes 0~3 is provided in Table 43.7-1, and can be changed according to the path delay in the application.

Table 43.7-1. Clock Phase and Polarity Configuration as Master

| Control Bit       | Mode 0 | Mode 1 | Mode 2 | Mode 3 |
|-------------------|--------|--------|--------|--------|
| SPI_CK_IDLE_EDGE  | 0      | 0      | 1      | 1      |
| SPI_CK_OUT_EDGE   | 0      | 1      | 1      | 0      |

☐SPI_CLK_MODE is used to select the number of rising edges of SPI_CLK when SPI_CS raises high to be 0, 1, 2 or SPI_CLK always on.
```