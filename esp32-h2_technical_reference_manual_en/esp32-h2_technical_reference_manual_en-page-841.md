

```markdown
| PARAMETER | SYMBOL | STANDARD-MODE MIN. MAX. | FAST-MODE MIN. MAX. | UNIT |
|:-----------------------------------------------------------------------------------------------------------------------------|:--------|:-------------------------|:--------------------|:------|
| SCL clock frequency | fSCL | 0 100 | 0 400 | kHz |
| Hold time (repeated) START condition. After this period, the first clock pulse is generated | tHD:STA | 4.0 | – | μs |
| LOW period of the SCL clock | tLOW | 4.7 | – | μs |
| HIGH period of the SCL clock | tHIGH | 4.0 | – | μs |
| Set-up time for a repeated START condition | tSU:STA | 4.7 | – | μs |
| Data hold time: for CBUS compatible masters (see NOTE, Section 10.1.3) for I²C-bus devices | tHD:DAT | 5.0<br>0(2) | –<br>3.45(3)<sup>(2)</sup><br>–<br>0(2)<sup>(4)</sup> | μs |
| Data set-up time | tSU:DAT | 250 | – | ns |
| Rise time of both SDA and SCL signals | tr | – | 1000<br>300 | 20 + 0.1Cb<sup>(5)</sup><br>20 + 0.1Cb<sup>(5)</sup> | ns |
| Fall time of both SDA and SCL signals | tf | – | 300 | 20 + 0.1Cb<sup>(5)</sup> | ns |
| Set-up time for STOP condition | tSU:STO | 4.0 | – | μs |
| Bus free time between a STOP and START condition | tBUF | 4.7 | – | μs |

Table 30.3-1. I2C Timing Parameters (Cited from Table 5 in The I²C-bus specification Version 2.1)
```

## 30.4 Functional Description

As mentioned above, one or more masters and one or more slaves can be mounted on the I2C bus. The following sections describe the operations of the ESP32-H2 I2C controller. Note that operations may differ between the I2C controller in ESP32-H2 and other masters or slaves on the bus. Please refer to datasheets of individual I2C devices for specific information.

### 30.4.1 Clock Configuration

Registers, TX RAM, and RX RAM are configured and accessed in the APB_CLK clock domain. The main logic of the I2C controller, including SCL_FSM, SCL_MAIN_FSM, SCL_FILTER, SDA_FILTER, and DATA_SHIFTER, are in the I2C_SCLK clock domain.

You can choose the clock source for I2C_SCLK from XTAL_CLK or RC_FAST_CLK via `PCR_I2C_SCLK_SEL`:

* Enable the clock source for I2C_SCLK by configuring `PCR_I2C_SCLK_EN` to 1.
* When `PCR_I2C_SCLK_SEL` is 0, the clock source is XTAL_CLK.
* When `PCR_I2C_SCLK_SEL` is 1, the clock source is RC_FAST_CLK.

The clock source then passes through a fractional divider to generate I2C_SCLK according to the following equation:

```latex
Divisor = PCR_I2C_SCLK_DIV_NUM + 1 + \frac{PCR_I2C_SCLK_DIV_A}{PCR_I2C_SCLK_DIV_B}
```

Limited by timing parameters, the derived clock I2C_SCLK should operate at a frequency 20 times larger than SCL's frequency.
```