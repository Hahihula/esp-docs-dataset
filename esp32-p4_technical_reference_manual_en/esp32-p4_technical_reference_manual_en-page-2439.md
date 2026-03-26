
```markdown
Chapter 45 Analog I2C Controller

## Chapter 45

### Analog I2C Controller

#### 45.1 Introduction

The Analog I2C Controller contains two I2C masters dedicated to configuring and communicating with certain analog circuit modules. Those modules can adjust their operating states by configuring their internal registers to better suit the current application scenario of the chip. For example, the Analog I2C Controller can configure an analog sensor to add a uniform offset to the ADC sampling values, thereby extending the sampling voltage range. Each configurable analog module has an I2C slave internally, which is assigned with an independent address. The Analog I2C Controller supports the configuration of the following analog modules:

*   CPU_PLL: This mainly includes the configuration register for CPLL_CLK, with a slave address of 0x67. For more information on CPLL_CLK, refer to Chapter 10 Reset and Clock.
*   SYS_PLL: This mainly includes the configuration register for SPLL_CLK, with a slave address of 0x66. For more information on SPLL_CLK, refer to Chapter 10 Reset and Clock.
*   MSPI: This mainly includes the configuration register for MPLL_CLK , with a slave address of 0x63. For more information on MPLL_CLK, refer to Chapter 10 Reset and Clock.
*   PLLA: This mainly includes the configuration register for APLL_CLK , with a slave address of 0x6f. For more information on APLL_CLK, refer to Chapter 10 Reset and Clock.
*   ANA_SENSOR: This mainly includes the configuration register for analog sensors (such as Temperature Sensor (TSENS) and ADC Controller (ADC)), with a slave address of 0x69.
*   BIAS: This mainly includes the voltage detection configuration register, with a slave address of 0x6a. For more information, refer to Chapter 23 Brown-out Detector.

#### 45.2 Feature List

The Analog I2C Controller has the following features:

*   Master mode only
*   7-bit addressing
*   Adjustable transmission rate
*   Communication in the sleep modes supported by the Low-Power CPU
*   Dual master operation mode
```