

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **Configuration Register**                 |                                                                                  |           |        |
| LEDC_CHO_CONF0_REG                        | Configuration register 0 for channel 0                                                           | 0x0000    | varies |
| LEDC_CHO_CONF1_REG                        | Configuration register 1 for channel 0                                                           | 0x000C    | varies |
| LEDC_CH1_CONF0_REG                        | Configuration register 0 for channel 1                                                           | 0x0014    | varies |
| LEDC_CH1_CONF1_REG                        | Configuration register 1 for channel 1                                                           | 0x0020    | varies |
| LEDC_CH2_CONF0_REG                        | Configuration register 0 for channel 2                                                           | 0x0028    | varies |
| LEDC_CH2_CONF1_REG                        | Configuration register 1 for channel 2                                                           | 0x0034    | varies |
| LEDC_CH3_CONF0_REG                        | Configuration register 0 for channel 3                                                           | 0x003C    | varies |
| LEDC_CH3_CONF1_REG                        | Configuration register 1 for channel 3                                                           | 0x0048    | varies |
| LEDC_CH4_CONF0_REG                        | Configuration register 0 for channel 4                                                           | 0x0050    | varies |
| LEDC_CH4_CONF1_REG                        | Configuration register 1 for channel 4                                                           | 0x005C    | varies |
| LEDC_CH5_CONF0_REG                        | Configuration register 0 for channel 5                                                           | 0x0064    | varies |
| LEDC_CH5_CONF1_REG                        | Configuration register 1 for channel 5                                                           | 0x0070    | varies |
| LEDC_CONF_REG                             | Global LEDC configuration register                                                              | 0x00D0    | R/W    |
| **Hpoint Register**                       |                                                                                  |           |        |
| LEDC_CHO_HPOINT_REG                       | High point register for channel 0                                                               | 0x0004    | R/W    |
| LEDC_CH1_HPOINT_REG                       | High point register for channel 1                                                               | 0x0018    | R/W    |
| LEDC_CH2_HPOINT_REG                       | High point register for channel 2                                                               | 0x002C    | R/W    |
| LEDC_CH3_HPOINT_REG                       | High point register for channel 3                                                               | 0x0040    | R/W    |
| LEDC_CH4_HPOINT_REG                       | High point register for channel 4                                                               | 0x0054    | R/W    |
| LEDC_CH5_HPOINT_REG                       | High point register for channel 5                                                               | 0x0068    | R/W    |
| **Duty Cycle Register**                   |                                                                                  |           |        |
| LEDC_CHO_DUTY_REG                         | Initial duty cycle for channel 0                                                                | 0x0008    | R/W    |
| LEDC_CHO_DUTY_R_REG                       | Current duty cycle for channel 0                                                                | 0x0010    | RO     |
| LEDC_CH1_DUTY_REG                         | Initial duty cycle for channel 1                                                                | 0x001C    | R/W    |
| LEDC_CH1_DUTY_R_REG                       | Current duty cycle for channel 1                                                                | 0x0024    | RO     |
| LEDC_CH2_DUTY_REG                         | Initial duty cycle for channel 2                                                                | 0x0030    | R/W    |
| LEDC_CH2_DUTY_R_REG                       | Current duty cycle for channel 2                                                                | 0x0038    | RO     |
| LEDC_CH3_DUTY_REG                         | Initial duty cycle for channel 3                                                                | 0x0044    | R/W    |
| LEDC_CH3_DUTY_R_REG                       | Current duty cycle for channel 3                                                                | 0x004C    | RO     |
| LEDC_CH4_DUTY_REG                         | Initial duty cycle for channel 4                                                                | 0x0058    | R/W    |
| LEDC_CH4_DUTY_R_REG                       | Current duty cycle for channel 4                                                                | 0x0060    | RO     |
| LEDC_CH5_DUTY_REG                         | Initial duty cycle for channel 5                                                                | 0x006C    | R/W    |
| LEDC_CH5_DUTY_R_REG                       | Current duty cycle for channel 5                                                                | 0x0074    | RO     |
| **Timer Register**                        |                                                                                  |           |        |
| LEDC_TIMERO_CONF_REG                       | Timer 0 configuration                                                                            | 0x00A0    | varies |
| LEDC_TIMERO_VALUE_REG                     | Timer 0 current counter value                                                                     | 0x00A4    | RO     |
```