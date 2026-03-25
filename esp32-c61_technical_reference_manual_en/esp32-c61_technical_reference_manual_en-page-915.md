

```markdown
SCK and sampled on the falling edge.

3. Mode 2: CPOL = 1, CPHA = 0; SCK is 1 when the SPI is in idle state; data is changed on the rising edge of SCK and sampled on the falling edge. The first data is shifted out before the first rising edge of SCK.

4. Mode 3: CPOL = 1, CPHA = 1; SCK is 1 when the SPI is in idle state; data is changed on the falling edge of SCK and sampled on the rising edge.
```

## 26.7.2 Clock Control When GP-SPI2 Works as Master

The four clock modes 0~3 are supported in GP-SPI2 when it works as master. The polarity and phase of GP-SPI2 clock are controlled by the bit `SPI_CK_IDLE_EDGE` in register `SPI_MISC_REG` and the bit `SPI_CK_OUT_EDGE` in register `SPI_USER_REG`. The register configuration for SPI clock modes 0~3 is provided in Table 26.7-1, and can be changed according to the path delay in the application.

**Table 26.7-1. Clock Phase and Polarity Configuration as Master**

| Control Bit     | Mode 0 | Mode 1 | Mode 2 | Mode 3 |
|-----------------|--------|--------|--------|--------|
| SPI_CK_IDLE_EDGE | 0      | 0      | 1      | 1      |
| SPI_CK_OUT_EDGE  | 0      | 1      | 1      | 0      |

`SPI_CLK_MODE` is used to select the number of rising edges of SPI_CLK when `SPI_CS` raises high to be 0, 1, 2 or `SPI_CLK` always on.

**Note:**
When `SPI_CLK_MODE` is configured to 1 or 2, the bit `SPI_CS_HOLD` must be set and the value of `SPI_CS_HOLD_TIME` should be larger than 1.

## 26.7.3 Clock Control When GP-SPI2 Works as Slave

GP-SPI2 as slave also supports clock modes 0~3. The polarity and phase are configured by the bits `SPI_TSCK_I_EDGE` and `SPI_RSCK_I_EDGE` in register `SPI_USER_REG`. The output edge of data is controlled by `SPI_CLK_MODE_13` in register `SPI_SLAVE_REG`. The detailed register configuration is shown in Table 26.7-2:

**Table 26.7-2. Clock Phase and Polarity Configuration as Slave**

| Control Bit     | Mode 0 | Mode 1 | Mode 2 | Mode 3 |
|-----------------|--------|--------|--------|--------|
| SPI_TSCK_I_EDGE | 0      | 1      | 1      | 0      |
| SPI_RSCK_I_EDGE | 0      | 1      | 1      | 0      |
| SPI_CLK_MODE_13 | 0      | 1      | 0      | 1      |

## 26.8 GP-SPI2 Timing Compensation

### Introduction

Based on the role of GP-SPI2 in a user-defined SPI transmission system (whether GP-SPI2 works as master or slave), GP-SPI2 provides the following timing compensation schemes:
```