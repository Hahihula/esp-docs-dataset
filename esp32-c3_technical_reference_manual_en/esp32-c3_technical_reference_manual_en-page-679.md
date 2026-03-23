

```markdown
| PARAMETER | SYMBOL | STANDARD-MODE MIN. MAX. | FAST-MODE MIN. MAX. | UNIT |
|:-----------------------------------------------------------------------------------------------------------------------------|:--------|:-------------------------|:--------------------|:------|
| SCL clock frequency | fSCL | 0 100 | 0 400 | kHz |
| Hold time (repeated) START condition. After this period, the first clock pulse is generated | tHD:STA | 4.0 | – | – | μs |
| LOW period of the SCL clock | tLOW | 4.7 | – | – | μs |
| HIGH period of the SCL clock | tHIGH | 4.0 | – | – | μs |
| Set-up time for a repeated START condition | tSU:STA | 4.7 | – | – | μs |
| Data hold time: for CBUS compatible masters (see NOTE, Section 10.1.3) for I²C-bus devices | tHD:DAT | 5.0 <br> 0(2) | –<br> 3.45(3) | –<br> 0(2)<sup>(4)</sup> | μs<br> μs |
| Data set-up time | tSU:DAT | 250 | – | – | ns |
| Rise time of both SDA and SCL signals | tr | – | 1000 | 20 + 0.1Cb<sup>(5)</sup> | ns |
| Fall time of both SDA and SCL signals | tf | – | 300 | 20 + 0.1Cb<sup>(5)</sup> | ns |
| Set-up time for STOP condition | tSU:STO | 4.0 | – | – | μs |
| Bus free time between a STOP and START condition | tBUF | 4.7 | – | – | μs |

Figure 28.3-4. I2C Timing Parameters (Cited from Table 5 in The I2C-bus specification Version 2.1)
```

## 28.4 Functional Description

Note that operations may differ between the I2C controller in ESP32-C3 and other masters or slaves on the bus. Please refer to datasheets of individual I2C devices for specific information.

### 28.4.1 Clock Configuration

Registers, TX RAM, and RX RAM are configured and accessed in the APB_CLK clock domain, whose frequency is 1 ~ 80 MHz. The main logic of the I2C controller, including SCL_FSM, SCL_MAIN_FSM, SCL_FILTER, SDA_FILTER, and DATA_SHIFTER, are in the I2C_SCL clock domain.

You can choose the clock source for I2C_SCL from XTAL_CLK or RC_FAST_CLK via I2C_SCL_SEL. When I2C_SCL_SEL is cleared, the clock source is XTAL_CLK. When I2C_SCL_SEL is set, the clock source is RC_FAST_CLK. The clock source is enabled by configuring I2C_SCL_ACTIVE as high level, and then passes through a fractional divider to generate I2C_SCL according to the following equation:

```latex
Divisor = \frac{I2C_SCL_DIV_NUM}{1} + 1 + \frac{I2C_SCL_DIV_A}{I2C_SCL_DIV_B}
```

The frequency of XTAL_CLK is 40 MHz, while the frequency of RC_FAST_CLK is 17.5 MHz. Limited by timing parameters, the derived clock I2C_SCL should operate at a frequency 20 timers larger than SCL's frequency.

### 28.4.2 SCL and SDA Noise Filtering

SCL_Filter and SDA_Filter modules are identical and are used to filter signal noises on SCL and SDA, respectively. These filters can be enabled or disabled by configuring I2C_SCL_FILTER_EN and I2C_SDA_FILTER_EN.
```