

```markdown
| PARAMETER | SYMBOL | STANDARD-MODE MIN. MAX. | FAST-MODE MIN. MAX. | UNIT |
|:-----------------------------------------------------------------------------------------------------------------------------|:--------|:-------------------------|:--------------------|:------|
| SCL clock frequency | fSCL | 0 100 0 | 400 kHz |  |
| Hold time (repeated) START condition. After this period, the first clock pulse is generated | tHD;STA | 4.0 – | 0.6 – | μs |
| LOW period of the SCL clock | tLOW | 4.7 – | 1.3 – | μs |
| HIGH period of the SCL clock | tHIGH | 4.0 – | 0.6 – | μs |
| Set-up time for a repeated START condition | tSU;STA | 4.7 – | 0.6 – | μs |
| Data hold time: for CBUS compatible masters (see NOTE, Section 10.1.3) for I²C-bus devices | tHD;DAT | 5.0 <br> 0(2) – | 3.45(3) <br> –<br> 0(2)–(4) | μs |
| Data set-up time | tSU;DAT | 250 – | 100 –(4) | ns |
| Rise time of both SDA and SCL signals | tr | – 1000 | 20 + 0.1Cb(5) <br> 300 | ns |
| Fall time of both SDA and SCL signals | tf | – 300 | 20 + 0.1Cb(5) <br> 300 | ns |
| Set-up time for STOP condition and | tSU;STO | 4.0 – | 0.6 – | μs |
| Bus free time between a STOP | tBUF | 4.7 – | 1.3 – | μs |
```

## 27.4 Functional Description

As mentioned above, one or more masters and one or more slaves can be connected on the I²C bus. The following sections describe the operations of the ESP32-C61 I²C controller. Note that operations may differ between the I²C controller in ESP32-C61 and other masters or slaves on the bus. Please refer to datasheets of individual I²C devices for specific information.

### 27.4.1 Clock Configuration

Registers, TX RAM, and RX RAM are configured and accessed in the APB_CLK clock domain. The main logic of the I²C controller, including SCL_FSM, SCL_MAIN_FSM, SCL_FILTER, SDA_FILTER, and DATA_SHIFTER, are in the I2C_SCLK clock domain.
```