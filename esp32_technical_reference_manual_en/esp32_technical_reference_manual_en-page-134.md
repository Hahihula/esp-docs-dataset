**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Section Header with Back Link:**
GoBack

**Note:**
- Pin can only be configured as input GPIO. These input-only pins do not feature an output driver or internal pull-up/pull-down circuitry.

**Reference to Document Section for More Details:**
Please refer to the ESP32 Pin Lists in ESP32 Series Datasheet for more details.
GoBack

**Subsection Title and Table Header with Description:**
6.11 RTC_MUX Pin List
Table 6.11-1 shows the RTC pins and how they correspond to GPIO pins:
Table Summary - 6.11-1. RTC IO MUX Pin Summary

| RTC GPIO Num | GPIO Num | Pin Name       | Analog Function | RTC Function |
|--------------|----------|----------------|-----------------|-------------|
|              |          |                |                 |             |
| 0            | 36       | SENSOR_VP     | ADC_H           | -           |
|              |          |                | ADC1_CHO        | RTC_GPIO00  |
| 1            | 37       | SENSOR_CAPP   | ADC_H           | ADC1_CH1    | RTC_GPIO1 |
|              |          |                | ADC1_CH2        | RTC_GPIO2   |
| 2            | 38       | SENSOR_CAPN   | ADC_H           | ADC1_CH3    | RTC_GPIO3 |
|              |          |                | ADC1_CH4        | RTC_GPIO4   |
| 3            | 39       | SENSOR_VN     | ADC_H           | ADC1_CH5    | RTC_GPIO5 |
|              |          |                | ADC1_CH6        | RTC_GPIO6   |
| 4            | 34       | VDEI_1        | -               | -           |
|              |          |                | ADC2_CHO        | RTC_GPIO7   |
| 5            | 35       | VDEI_2        | -               | -           |
|              |          |                | ADC2_CH1        | RTC_GPIO8   |
| 6            | 25       | GPIO25        | DAC_1           | ADC2_CH2    | RTC_GPIO9 |
|              |          |                | ADC2_CH3        | RTC_GPIO10  |
| 7            | 26       | GPIO26        | DAC_2           | ADC2_CH4    | RTC_GPIO11 |
|              |          |                | ADC2_CH5        | RTC_GPIO12  |
| 8            | 33       | 32K_XN       | XTAL_32K_N     | -           |
|              |          |                | ADC1_CH6        | I2C_SCL*    |
| 9            | 32       | 32K_XP       | XTAL_32K_P     | ADC1_CH7    | RTC_GPIO14 |
|              |          |                | ADC2_CHO        | -           |
| 10           | 4        | GPIO4         | -               | I2C_SDA*    |
|              |          |                | ADC2_CH1        | -           |
| 11           | 0        | GPIO0         | -               | -           |
|              |          |                | ADC2_CHO        | -           |
| 12           | 2        | GPIO2         | -               | I2C_SDA*    |
|              |          |                | ADC2_CH2        | -           |
| 13           | 15       | MTDO          | -               | -           |
|              |          |                | ADC2_CH3        | -           |
| 14           | 13       | MTCK          | -               | -           |
|              |          |                | ADC2_CH4        | -           |
| 15           | 12       | MTDI          | -               | -           |
|              |          |                | ADC2_CH5        | -           |
| 16           | 14       | MTMS          | -               | -           |
|              |          |                | ADC2_CHO        | -           |
| 17           | 27       | GPIO27        | -               | -           |

**Note:**
For more information on the configuration of sar_i2c_xx, see Section RTC I2C Controller in Chapter 1 ULP Coprocessor (ULP).

**Subsection Title and Table Header with Description for Another Register Summary:**
6.12 Register Summary
Table 6.12-1. GPIO Matrix Register Summary

| Name          | Description                   | Address       | Access |
|---------------|-------------------------------|---------------|--------|
| GPIO_OUT_REG  | GPIO O-31 output register     | 0x3FF44004   | R/W    |

**Footer:**
Espressif Systems
Page Number and Document Version:
134 ESP32 TRM (Version 5.6)
Submit Documentation Feedback