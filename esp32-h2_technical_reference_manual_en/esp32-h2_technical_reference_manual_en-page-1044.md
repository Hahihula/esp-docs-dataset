

```markdown
## 35.5 Registers

The addresses in this section are relative to LED PWM Controller base address provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 35.1. LEDC_CHn_CONFO_REG (n: 0-5) (0x0000+0x14*n)

| Bit | Description |
|-----|-------------|
| 31  | reserved    |
| 30  | Reset       |
| 29  | LEDC_TIMER_SEL_CHn Configures the timer for channel n. <br> O: timer 0 <br> 1: timer 1 <br> 2: timer 2 <br> 3: timer 3 (R/W) |
| 28  | LEDC_SIG_OUT_EN_CHn Configures whether or not to enable signal output on channel n. <br> O: Disable <br> 1: Enable (R/W) |
| 27  | LEDC_IDLE_LV_CHn Configures the output level when channel n is inactive (when LEDC_SIG_OUT_EN_CHn is 0). (R/W) |
| 26  | LEDC_PARA_UP_CHn Configures whether or not to update LEDC_HPOINT_CHn, LEDC_DUTY_START_CHn, LEDC_SIG_OUT_EN_CHn, LEDC_TIMER_SEL_CHn, and LEDC_OVF_CNT_ENT_CHn fields for channel n. <br> O: Invalid. No effect <br> 1: Update (WT) |
| 25  | LEDC_OVF_NUM_CHn Configures the maximum overflow times minus 1. The LEDC_OVF_CNT_CHn_INT interrupt will be triggered when channel n overflows for LEDC_OVF_NUM_CHn + 1 times. (R/W) |
| 24  | LEDC_OVF_CNT_ENT_CHn Configures whether or not to enable the overflow counter of channel n. <br> O: Disable <br> 1: Enable (R/W) |

Continued on the next page...
```