
```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| LEDC_CH2_DUTY_REG                          | Initial duty cycle for channel 2                                           | 0x0030  | R/W    |
| LEDC_CH2_DUTY_R_REG                        | Current duty cycle for channel 2                                            | 0x0038  | RO     |
| LEDC_CH3_DUTY_REG                          | Initial duty cycle for channel 3                                            | 0x0044  | R/W    |
| LEDC_CH3_DUTY_R_REG                        | Current duty cycle for channel 3                                            | 0x004C  | RO     |
| LEDC_CH4_DUTY_REG                          | Initial duty cycle for channel 4                                            | 0x0058  | R/W    |
| LEDC_CH4_DUTY_R_REG                        | Current duty cycle for channel 4                                            | 0x0060  | RO     |
| LEDC_CH5_DUTY_REG                          | Initial duty cycle for channel 5                                            | 0x006C  | R/W    |
| LEDC_CH5_DUTY_R_REG                        | Current duty cycle for channel 5                                            | 0x0074  | RO     |

**Timer Register**

| Name                                       | Description                                                                 | Address | Access   |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|----------|
| LEDC_TIMERO_CONF_REG                       | Timer 0 configuration                                                       | 0x00AO  | varies   |
| LEDC_TIMERO_VALUE_REG                      | Timer 0 current counter value                                               | 0x00A4  | RO       |
| LEDC_TIMER1_CONF_REG                       | Timer 1 configuration                                                       | 0x00A8  | varies   |
| LEDC_TIMER1_VALUE_REG                      | Timer 1 current counter value                                               | 0x00AC  | RO       |
| LEDC_TIMER2_CONF_REG                       | Timer 2 configuration                                                       | 0x00BO  | varies   |
| LEDC_TIMER2_VALUE_REG                      | Timer 2 current counter value                                               | 0x00B4  | RO       |
| LEDC_TIMER3_CONF_REG                       | Timer 3 configuration                                                       | 0x00B8  | varies   |
| LEDC_TIMER3_VALUE_REG                      | Timer 3 current counter value                                               | 0x00BC  | RO       |

**Interrupt Register**

| Name                                       | Description                                                                 | Address | Access     |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|------------|
| LEDC_INT_RAW_REG                           | Raw interrupt status                                                        | 0x00CO  | R/WTC/SS   |
| LEDC_INT_ST_REG                             | Masked interrupt status                                                     | 0x00C4  | RO         |
| LEDC_INT_ENA_REG                            | Interrupt enable bits                                                       | 0x00C8  | R/W        |
| LEDC_INT_CLR_REG                            | Interrupt clear bits                                                        | 0x00CC  | WT         |

**Gamma RAM Register**

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| LEDC_CHO_GAMMA_WR_REG                      | LEDC channel 0 gamma RAM write register                                    | 0x0100  | R/W    |
| LEDC_CHO_GAMMA_WR_ADDR_REG                 | LEDC channel 0 gamma RAM write address register                            | 0x0104  | R/W    |
| LEDC_CHO_GAMMA_RD_ADDR_REG                 | LEDC channel 0 gamma RAM read address register                             | 0x0108  | R/W    |
| LEDC_CHO_GAMMA_RD_DATA_REG                 | LEDC channel 0 gamma RAM read data register                                | 0x010C  | RO     |
| LEDC_CH1_GAMMA_WR_REG                      | LEDC channel 1 gamma RAM write register                                    | 0x0110  | R/W    |
| LEDC_CH1_GAMMA_WR_ADDR_REG                 | LEDC channel 1 gamma RAM write address register                            | 0x0114  | R/W    |
| LEDC_CH1_GAMMA_RD_ADDR_REG                 | LEDC channel 1 gamma RAM read address register                             | 0x0118  | R/W    |
| LEDC_CH1_GAMMA_RD_DATA_REG                 | LEDC channel 1 gamma RAM read data register                                | 0x011C  | RO     |
| LEDC_CH2_GAMMA_WR_REG                      | LEDC channel 2 gamma RAM write register                                    | 0x0120  | R/W    |
| LEDC_CH2_GAMMA_WR_ADDR_REG                 | LEDC channel 2 gamma RAM write address register                            | 0x0124  | R/W    |
| LEDC_CH2_GAMMA_RD_ADDR_REG                 | LEDC channel 2 gamma RAM read address register                             | 0x0128  | R/W    |
| LEDC_CH2_GAMMA_RD_DATA_REG                 | LEDC channel 2 gamma RAM read data register                                | 0x012C  | RO     |
```