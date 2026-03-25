

```markdown
| PARAMETER | SYMBOL | STANDARD-MODE MIN. MAX. | FAST-MODE MIN. MAX. | UNIT |
|:-----------------------------------------------------------------------------------------------------------------------------|:--------|:-------------------------|:--------------------|:------|
| SCL clock frequency | fSCL | 0 100 | 0 400 | kHz |
| Hold time (repeated) START condition. After this period, the first clock pulse is generated | tHD:STA | 4.0 | – | – | μs |
| LOW period of the SCL clock | tLOW | 4.7 | – | – | μs |
| HIGH period of the SCL clock | tHIGH | 4.0 | – | – | μs |
| Set-up time for a repeated START condition | tSU:STA | 4.7 | – | – | μs |
| Data hold time: for CBUS compatible masters (see NOTE, Section 10.1.3) for I²C-bus devices | tHD:DAT | 5.0<br>0(2) | –<br>3.45(3)<sup>(2)</sup> | –<br>0.9(3) | μs |
| Data set-up time | tSU:DAT | 250 | – | – | ns |
| Rise time of both SDA and SCL signals | tr | – | 1000<br>– | 20 + 0.1Cb<sup>(5)</sup><br>300 | ns |
| Fall time of both SDA and SCL signals | tf | – | 300<br>– | 20 + 0.1Cb<sup>(5)</sup><br>300 | ns |
| Set-up time for STOP condition | tSU:STO | 4.0 | – | – | μs |
| Bus free time between a STOP and START condition | tBUF | 4.7 | – | – | μs |

Table 34.3-1. I2C Timing Parameters (Cited from Table 5 in The I²C-bus specification Version 2.1)
```

## 34.4 Functional Description

As mentioned above, one or more masters and one or more slaves can be connected on the I2C bus. The following sections describe the operations of the ESP32-C5 I2C controllers. Note that operations may differ between the I2C controllers in ESP32-C5 and other masters or slaves on the bus. Please refer to datasheets of individual I2C devices for specific information.

### 34.4.1 Clock Configuration

Registers, TX RAM, and RX RAM are configured and accessed in the APB_CLK clock domain. The main logic of the I2C controller, including SCL_FSM, SCL_MAIN_FSM, SCL_FILTER, SDA_FILTER, and DATA_SHIFTER, are in the I2C_SCLK clock domain.

You can configure the clock source for I2C_SCLK of I2C in the main system (HP) to XTAL_CLK or RC_FAST_CLK via `PCR_I2C_SCLK_SEL`. For the clock source for I2C_SCLK of LP_I2C in the low-power system (LP), you can configure it to CLK_XTALD2 or CLK_ROOT_FAST via LP_CLKRST_LP_I2C_CLK_SEL.

The steps to configure the clock source for I2C are as follows:

*   Enable the clock source for I2C_SCLK of I2C by configuring `PCR_I2C_SCLK_EN` to 1.
*   When `PCR_I2C_SCLK_SEL` is 0, the clock source is XTAL_CLK.
*   When `PCR_I2C_SCLK_SEL` is 1, the clock source is RC_FAST_CLK.

The steps to configure the clock source for LP_I2C are as follows:

*   Enable the clock source for I2C_SCLK of LP_I2C by configuring LPPERI_LP_EXT_I2C_CK_EN to 1.
*   When `LP_CLKRST_LP_I2C_CLK_SEL` is 0, the clock source is CLK_ROOT_FAST.
*   When `LP_CLKRST_LP_I2C_CLK_SEL` is 1, the clock source is CLK_XTALD2.
```