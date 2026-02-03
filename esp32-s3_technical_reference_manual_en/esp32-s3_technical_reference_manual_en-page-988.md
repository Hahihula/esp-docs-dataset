**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Table of Parameters and Values for Standard-Mode vs Fast-Mode**

| PARAMETER                   | SYMBOL       | STANDARD-MODE MIN. | STANDARD-MODE MAX. | FAST-MODE MIN. | FAST-MODE MAX. | UNIT    |
|-----------------------------|--------------|--------------------|--------------------|----------------|----------------|---------|
| SCL clock frequency         | fSCL         | 0                  | 100                | 400            | -              | kHz     |
| Hold time (repeated) START condition. After this period, the first clock pulse is generated | tHD;STA      | 4.0                | –                 | –              | μs       |
| LOW period of the SCL clock | tLOW         | 4.7                | -                  | 1.3            | –              | μs       |
| HIGH period of the SCL clock | tHIGH        | 4.0                | 0.6               | –              | –              | μs       |
| Set-up time for a repeated START condition | tSU;STA      | 4.7                | -                  | 0.6            | –              | μs       |
| Data hold time: for CBUS compatible masters (see NOTE, Section 10.1.3) for I2C-bus devices | tHD;DAT      | 5.0                | –                  | –              | μs         |
| Data set-up time            | tSU;DAT      | 250               | 3.45(3)           | (0.9)(3)       | ns             |
| Rise time of both SDA and SCL signals | tr          | -                  | –                 | 1000           | 20 + 0.1Cb(5) | ns       |
| Fall time of both SDA and SCL signals | tf          | 300               | (20 + 0.1Cb)(5)   | 300            | ns             |
| Set-up time for STOP condition | tSU;STO      | –                  | -                 | 4.7            | μs             |
| Bus free time between a STOP and START condition | tBUF        | (STOP + 1.3)       | –                 | –              | μs           |

**Figure Caption:**
Figure 27.3-4. I2C Timing Parameters (Cited from Table 5 in The I2C-bus specification Version 2.1)

**Section Title and Subsections with Content**

**27.4 Functional Description**

Note that operations may differ between the I2C controller in ESP32-S3 and other masters or slaves on the bus. Please refer to datasheets of individual I2C devices for specific information.

**27.4.1 Clock Configuration**

Registers, TX RAM, and RX RAM are configured and accessed in the APB_CLK clock domain, whose frequency is 1 ~ 80 MHz. The main logic of the I2C controller, including SCL FSM, SCL_MAIN FSM, SCL_FILTER, SDA_FILTER, and DATA_SHIFTER, are in the I2C-SCLK clock domain.

You can choose the clock source for I2C-SCLK from XTAL_CLK or RC_FAST_CLK via I2C_SCLK_SEL. When I2C_SCLK_SEL is cleared, the clock source is XTAL_CLK. When I2C_SCLK_SEL is set, the clock source is RC_FAST_CLK. The clock source is enabled by configuring I2C_SCLK_ACTIVE as high level, and then passes through a fractional divider to generate I2C-SCLK according to the following equation:

\[ \text{Divisor} = \frac{\text{I2C_SCLK_DIV_NUM}}{\text{I2C_SCLK_DIV_Denominator}} + 1 + \frac{\text{I2C_SCLK_DIV_A}}{\text{I2C_SCLK_DIV_B}} \]

The frequency of XTAL_CLK is 40 MHz, while the frequency of RC_FAST_CLK is 17.5 MHz. Limited by timing parameters, the derived clock I2C_SCLK should operate at a frequency 20 times larger than SCL's frequency.

**27.4.2 SCL and SDA Noise Filtering**

SCL_Filter and SDA_Filter modules are identical and used to filter signal noises on SCL and SDA respectively. These filters can be enabled or disabled by configuring I2C_SCLK_FILTER_EN and I2C_SDA_FILTER_EN

**Footer:**
Espressif Systems
988 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback