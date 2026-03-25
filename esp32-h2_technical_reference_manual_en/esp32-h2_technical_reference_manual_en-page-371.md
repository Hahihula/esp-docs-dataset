

```markdown
SOC_ETM_CH_ENABLEn and SOC_ETM_CH_DISABLEn are used to enable or disable channeln.
SOC_ETM_CH_ENABLEDn is used to indicate the status of the channeln.

10.3.2 Events

An ETM channel can be set up to choose which event to receive by configuring the SOC_ETM_CHn_EVT_ID field.
Table 10.3-1 shows the configuration values of SOC_ETM_CHn_EVT_ID and their corresponding events.

Table 10.3-1. Selectable Events for ETM Channeln

| SOC_ETM_CHn_EVT_ID | Selected Event                                 | Peripheral Generating This Event |
|--------------------|------------------------------------------------|----------------------------------|
| 1                  | GPIO_EVT_CHO_RISE_EDGE                        | GPIO                           |
| 2                  | GPIO_EVT_CH1_RISE_EDGE                        |                                  |
| 3                  | GPIO_EVT_CH2_RISE_EDGE                        |                                  |
| 4                  | GPIO_EVT_CH3_RISE_EDGE                        |                                  |
| 5                  | GPIO_EVT_CH4_RISE_EDGE                        |                                  |
| 6                  | GPIO_EVT_CH5_RISE_EDGE                        |                                  |
| 7                  | GPIO_EVT_CH6_RISE_EDGE                        |                                  |
| 8                  | GPIO_EVT_CH7_RISE_EDGE                        |                                  |
| 9                  | GPIO_EVT_CHO_FALL_EDGE                        |                                  |
| 10                 | GPIO_EVT_CH1_FALL_EDGE                        |                                  |
| 11                 | GPIO_EVT_CH2_FALL_EDGE                        |                                  |
| 12                 | GPIO_EVT_CH3_FALL_EDGE                        |                                  |
| 13                 | GPIO_EVT_CH4_FALL_EDGE                        |                                  |
| 14                 | GPIO_EVT_CH5_FALL_EDGE                        |                                  |
| 15                 | GPIO_EVT_CH6_FALL_EDGE                        |                                  |
| 16                 | GPIO_EVT_CH7_FALL_EDGE                        |                                  |
| 17                 | GPIO_EVT_CHO_ANY_EDGE                         |                                  |
| 18                 | GPIO_EVT_CH1_ANY_EDGE                         |                                  |
| 19                 | GPIO_EVT_CH2_ANY_EDGE                         |                                  |
| 20                 | GPIO_EVT_CH3_ANY_EDGE                         |                                  |
| 21                 | GPIO_EVT_CH4_ANY_EDGE                         |                                  |
| 22                 | GPIO_EVT_CH5_ANY_EDGE                         |                                  |
| 23                 | GPIO_EVT_CH6_ANY_EDGE                         |                                  |
| 24                 | GPIO_EVT_CH7_ANY_EDGE                         |                                  |
| 25                 | LEDC_EVT_DUTY_CHNG_END_CHO                    | LED PWM Controller (LEDC)       |
| 26                 | LEDC_EVT_DUTY_CHNG_END_CH1                    |                                  |
| 27                 | LEDC_EVT_DUTY_CHNG_END_CH2                    |                                  |
| 28                 | LEDC_EVT_DUTY_CHNG_END_CH3                    |                                  |
| 29                 | LEDC_EVT_DUTY_CHNG_END_CH4                    |                                  |
| 30                 | LEDC_EVT_DUTY_CHNG_END_CH5                    |                                  |
| 31                 | LEDC_EVT_OVF_CNT_PLS_CHO                       |                                  |
| 32                 | LEDC_EVT_OVF_CNT_PLS_CH1                       |                                  |
| 33                 | LEDC_EVT_OVF_CNT_PLS_CH2                       |                                  |
| 34                 | LEDC_EVT_OVF_CNT_PLS_CH3                       |                                  |
| 35                 | LEDC_EVT_OVF_CNT_PLS_CH4                       |                                  |
```