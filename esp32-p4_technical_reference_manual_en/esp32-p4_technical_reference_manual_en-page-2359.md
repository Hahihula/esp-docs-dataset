

```markdown
| PARAMETER | SYMBOL | STANDARD-MODE MIN. MAX. | FAST-MODE MIN. MAX. | UNIT |
|:-----------------------------------------------------------------------------------------------------------------------------|:--------|:-------------------------|:--------------------|:------|
| SCL clock frequency | fSCL | 0 100 | 0 400 | kHz |
| Hold time (repeated) START condition. After this period, the first clock pulse is generated | tHD:STA | 4.0 | – | – | μs |
| LOW period of the SCL clock | tLOW | 4.7 | – | – | μs |
| HIGH period of the SCL clock | tHIGH | 4.0 | – | – | μs |
| Set-up time for a repeated START condition | tSU:STA | 4.7 | – | – | μs |
| Data hold time: for CBUS compatible masters (see NOTE, Section 10.1.3) for I²C-bus devices | tHD:DAT | 5.0<sup>(2)</sup> | – <br/> 3.45<sup>(3)</sup> | – <br/> 0.9<sup>(3)</sup> | μs |
| Data set-up time | tSU:DAT | 250 | – | – | ns |
| Rise time of both SDA and SCL signals | tr | – | 1000 | 20 + 0.1Cb<sup>(5)</sup> | ns |
| Fall time of both SDA and SCL signals | tf | – | 300 | 20 + 0.1Cb<sup>(5)</sup> | ns |
| Set-up time for STOP condition | tSU:STO | 4.0 | – | – | μs |
| Bus free time between a STOP and START condition | tBUF | 4.7 | – | – | μs |

Table 44.3-1. I2C Timing Parameters (Cited from Table 5 in The I²C-bus specification Version 2.1)
```

## 44.4 Functional Description

As mentioned above, one or more masters and one or more slaves can be connected on the I2C bus. The following sections describe the operations of the ESP32-P4 I2C controllers. Note that operations may differ between the I2C controllers in ESP32-P4 and other masters or slaves on the bus. Please refer to datasheets of individual I2C devices for specific information.

### 44.4.1 Clock Configuration

Registers, TX RAM, and RX RAM are configured and accessed in the APB_CLK clock domain. The main logic of the I2C controller, including SCL_FSM, SCL_MAIN_FSM, SCL_FILTER, SDA_FILTER, and DATA_SHIFTER, are in the I2C_SCLK clock domain.

You can configure the clock source for I2C_SCLK of I2CO in the main system (HP) to FOSC_2OM_CLK or XTAL_40M_CLK via HP_SYS_CLKRST_I2CO_CLK_SRC_SEL and configure that of I2C1 in the main system via HP_SYS_CLKRST_I2C1_CLK_SRC_SEL. For the clock source for I2C_SCLK of LP_I2C in the low-power system (LP), you can configure it to XTAL_D2_CLK, LP_DYN_FAST_CLK, or PLL_LP_CLK 8 MHz via LPPERI_LP_I2C_CLK_SEL.

The steps to configure the clock source for HP I2CO are as follows:

* Enable the clock source for I2C_SCLK of I2CO by configuring HP_SYS_CLKRST_I2CO_CLK_EN to 1.
* When HP_SYS_CLKRST_I2CO_SRC_SEL is 0, the clock source is XTAL_4OM_CLK.
* When HP_SYS_CLKRST_I2CO_SRC_SEL is 1, the clock source is FOSC_2OM_CLK.

The steps to configure the clock source for HP I2C1 are as follows:

* Enable the clock source for I2C_SCLK of I2C1 by configuring HP_SYS_CLKRST_I2C1_CLK_EN to 1.
```