

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LEDC_CHO_GAMMA_CONF_REG                   | LEDC channel 0 gamma config register                                      | 0x0100    | varies |
| LEDC_CH1_GAMMA_CONF_REG                   | LEDC channel 1 gamma config register                                      | 0x0104    | varies |
| LEDC_CH2_GAMMA_CONF_REG                   | LEDC channel 2 gamma config register                                      | 0x0108    | varies |
| LEDC_CH3_GAMMA_CONF_REG                   | LEDC channel 3 gamma config register                                      | 0x010C    | varies |
| LEDC_CH4_GAMMA_CONF_REG                   | LEDC channel 4 gamma config register                                      | 0x0110    | varies |
| LEDC_CH5_GAMMA_CONF_REG                   | LEDC channel 5 gamma config register                                      | 0x0114    | varies |
| LEDC_CH6_GAMMA_CONF_REG                   | LEDC channel 6 gamma config register                                      | 0x0118    | varies |
| LEDC_CH7_GAMMA_CONF_REG                   | LEDC channel 7 gamma config register                                      | 0x011C    | varies |
| LEDC_EVT_TASK_ENO_REG                     | LEDC event task enable bit register 0                                     | 0x0120    | R/W    |
| LEDC_EVT_TASK_EN1_REG                     | LEDC event task enable bit register 1                                     | 0x0124    | R/W    |
| LEDC_EVT_TASK_EN2_REG                     | LEDC event task enable bit register 2                                     | 0x0128    | R/W    |
| LEDC_TIMERO_CMP_REG                       | LEDC timer 0 compare value register                                      | 0x0140    | R/W    |
| LEDC_TIMER1_CMP_REG                       | LEDC timer 1 compare value register                                      | 0x0144    | R/W    |
| LEDC_TIMER2_CMP_REG                       | LEDC timer 2 compare value register                                      | 0x0148    | R/W    |
| LEDC_TIMER3_CMP_REG                       | LEDC timer 3 compare value register                                      | 0x014C    | R/W    |
| LEDC_CONF_REG                             | LEDC global configuration register                                       | 0x0170    | R/W    |

**Status Register**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LEDC_CHO_DUTY_R_REG                       | Current duty cycle register for channel 0                                 | 0x0010    | RO     |
| LEDC_CH1_DUTY_R_REG                       | Current duty cycle register for channel 1                                 | 0x0024    | RO     |
| LEDC_CH2_DUTY_R_REG                       | Current duty cycle register for channel 2                                 | 0x0038    | RO     |
| LEDC_CH3_DUTY_R_REG                       | Current duty cycle register for channel 3                                 | 0x004C    | RO     |
| LEDC_CH4_DUTY_R_REG                       | Current duty cycle register for channel 4                                 | 0x0060    | RO     |
| LEDC_CH5_DUTY_R_REG                       | Current duty cycle register for channel 5                                 | 0x0074    | RO     |
| LEDC_CH6_DUTY_R_REG                       | Current duty cycle register for channel 6                                 | 0x0088    | RO     |
| LEDC_CH7_DUTY_R_REG                       | Current duty cycle register for channel 7                                 | 0x009C    | RO     |
| LEDC_TIMERO_VALUE_REG                     | Timer 0 current counter value register                                    | 0x00A4    | RO     |
| LEDC_TIMER1_VALUE_REG                     | Timer 1 current counter value register                                    | 0x00AC    | RO     |
| LEDC_TIMER2_VALUE_REG                     | Timer 2 current counter value register                                    | 0x00B4    | RO     |
| LEDC_TIMER3_VALUE_REG                     | Timer 3 current counter value register                                    | 0x00BC    | RO     |
| LEDC_TIMERO_CNT_CAP_REG                   | LEDC timer 0 captured count value register                                | 0x0150    | RO     |
| LEDC_TIMER1_CNT_CAP_REG                   | LEDC timer 1 captured count value register                                | 0x0154    | RO     |
| LEDC_TIMER2_CNT_CAP_REG                   | LEDC timer 2 captured count value register                                | 0x0158    | RO     |
| LEDC_TIMER3_CNT_CAP_REG                   | LEDC timer 3 captured count value register                                | 0x015C    | RO     |

**Interrupt Register**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LEDC_INT_RAW_REG                           | Interrupt raw status register                                              | 0x00C0    | R/WTC/SS |
| LEDC_INT_ST_REG                            | Interrupt masked status register                                          | 0x00C4    | RO     |
| LEDC_INT_ENA_REG                           | Interrupt enable register                                                  | 0x00C8    | R/W    |
| LEDC_INT_CLR_REG                           | Interrupt clear register                                                   | 0x00CC    | WT     |

**Version Register**

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| LEDC_DATE_REG                              | Version control register                                                   | 0x0174    | R/W    |
```