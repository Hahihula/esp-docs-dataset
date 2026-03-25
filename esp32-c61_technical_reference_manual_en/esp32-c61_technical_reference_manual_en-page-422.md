

```markdown
Register 10.3. SOC_ETM_EVT_STO_REG (0x0A8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    | SOC_ETM_LEDC_EVT_DUTY_CHNG_END_CH3_ST | reserved) | SOC_ETM_LEDC_EVT_DUTY_CHNG_END_CH2_ST | SOC_ETM_LEDC_EVT_DUTY_CHNG_END_CH1_ST | SOC_ETM_LEDC_EVT_DUTY_CHNG_END_CH0_ST | SOC_ETM_GPIO_EVT_DET_ZERO | SOC_ETM_GPIO_EVT_DET_NEG | SOC_ETM_GPIO_EVT_CH4_ANY_POSO_ST | SOC_ETM_GPIO_EVT_CH4_ANY_EDGE_ST | SOC_ETM_GPIO_EVT_CH3_ANY_EDGE_ST | SOC_ETM_GPIO_EVT_CH2_ANY_EDGE_ST | SOC_ETM_GPIO_EVT_CH1_ANY_EDGE_ST | SOC_ETM_GPIO_EVT_CH0_ANY_EDGE_ST | SOC_ETM_GPIO_EVT_CH4_FALL_EDGE_ST | SOC_ETM_GPIO_EVT_CH3_FALL_EDGE_ST | SOC_ETM_GPIO_EVT_CH2_FALL_EDGE_ST | SOC_ETM_GPIO_EVT_CH1_FALL_EDGE_ST | SOC_ETM_GPIO_EVT_CH0_FALL_EDGE_ST | SOC_ETM_GPIO_EVT_CH4_RISE_EDGE_ST | SOC_ETM_GPIO_EVT_CH3_RISE_EDGE_ST | SOC_ETM_GPIO_EVT_CH2_RISE_EDGE_ST | SOC_ETM_GPIO_EVT_CH1_RISE_EDGE_ST | SOC_ETM_GPIO_EVT_CH0_RISE_EDGE_ST |
|     | 0  | 0  | 0  | 0  | 00 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

SOC_ETM_GPIO_EVT_CH0_RISE_EDGE_ST Represents GPIO_EVT_CH0_RISE_EDGE trigger status.
O: Not triggered
1: Triggered
(R/WTC/SS)

SOC_ETM_GPIO_EVT_CH1_RISE_EDGE_ST Represents GPIO_EVT_CH1_RISE_EDGE trigger status.
O: Not triggered
1: Triggered
(R/WTC/SS)

SOC_ETM_GPIO_EVT_CH2_RISE_EDGE_ST Represents GPIO_EVT_CH2_RISE_EDGE trigger status.
O: Not triggered
1: Triggered
(R/WTC/SS)

SOC_ETM_GPIO_EVT_CH3_RISE_EDGE_ST Represents GPIO_EVT_CH3_RISE_EDGE trigger status.
O: Not triggered
1: Triggered
(R/WTC/SS)

SOC_ETM_GPIO_EVT_CH4_RISE_EDGE_ST Represents GPIO_EVT_CH4_RISE_EDGE trigger status.
O: Not triggered
1: Triggered
(R/WTC/SS)
```