
```markdown
## 32.5 Registers

The addresses in this section are relative to LED PWM Controller base address provided in Table 3.3-3 in Chapter 3 System and Memory.

Register 32.1. LEDC_CHn_CONFO_REG (n: 0-5) (0x0000+20*n)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 17  | LEDC_OVF_CNT_RESET_CHn |
| 16  | LEDC_OVF_CNT_EN_CHn |
| 15  | LEDC_OVF_NUM_CHn |
| 5   | LEDC_PARA_UP_CHn |
| 4   | LEDC_IDLE_LV_CHn |
| 3   | LEDC_SIG_OUT_EN_CHn |
| 2   | LEDC_TIMER_SEL_CHn |
| 1   | Reset |
| 0   | Reset |

LEDC_TIMER_SEL_CHn This field is used to select one of the timers for channel n.
    0: select Timer0; 1: select Timer1; 2: select Timer2; 3: select Timer3 (R/W)

LEDC_SIG_OUT_EN_CHn Set this bit to enable signal output on channel n. (R/W)

LEDC_IDLE_LV_CHn This bit is used to control the output value when channel n is inactive (when LEDC_SIG_OUT_EN_CHn is 0). (R/W)

LEDC_PARA_UP_CHn This bit is used to update the listed fields below for channel n, and will be automatically cleared by hardware. (WT)
    * LEDC_HPOINT_CHn
    * LEDC_DUTY_START_CHn
    * LEDC_SIG_OUT_EN_CHn
    * LEDC_TIMER_SEL_CHn
    * LEDC_DUTY_NUM_CHn
    * LEDC_DUTY_CYCLE_CHn
    * LEDC_DUTY_SCALE_CHn
    * LEDC_DUTY_INC_CHn
    * LEDC_OVF_CNT_EN_CHn

LEDC_OVF_NUM_CHn This field is used to configure the maximum times of overflow minus 1.
The LEDC_OVF_CNT_CHn_INT interrupt will be triggered when channel n overflows for (LEDC_OVF_NUM_CHn + 1) times. (R/W)

LEDC_OVF_CNT_EN_CHn This bit is used to count the number of times when the timer selected by channel n overflows. (R/W)

LEDC_OVF_CNT_RESET_CHn Set this bit to reset the timer-overflow counter of channel n. (WT)
```