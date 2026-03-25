

```markdown
Register 40.1. LEDC_CHn_CONFO_REG (n: 0-5) (0x0000+0x14*n)

31                                 17 16 15 14                                    5 4 3 2 1 0
+--------------------------------------------------------------------------------------------------+
| (reserved) | LEDC_OVF_CNT_RESET_CHn | LEDC_OVF_CNT_EN_CHn | LEDC_OVF_NUM_CHn | LEDC_PARA_UP_CHn | LEDC_IDLE_LV_CHn | LEDC_SIG_OUT_EN_CHn | LEDC_TIMER_SEL_CHn |
+--------------------------------------------------------------------------------------------------+
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | 0 | Reset

LEDC_TIMER_SEL_CHn Configures which timer is channel n selected.
0: Select Timer 0
1: Select Timer 1
2: Select Timer 2
3: Select Timer 3
(R/W)

LEDC_SIG_OUT_EN_CHn Configures whether to enable signal output on channel n.
0: Signal output disable
1: Signal output enable
(R/W)

LEDC_IDLE_LV_CHn Configures the output value when channel n is inactive. Valid only when LEDC_SIG_OUT_EN_CHn is 0.
0: Output level is low
1: Output level is high
(R/W)

LEDC_PARA_UP_CHn Configures whether to update LEDC_HPOINT_CHn, LEDC_DUTY_START_CHn, LEDC_SIG_OUT_EN_CHn, LEDC_TIMER_SEL_CHn, LEDC_OVF_CNT_EN_CHn fields and duty cycle range configurations for channel n, and will be automatically cleared by hardware.
0: Invalid. No effect
1: Update
This bit is cleared by hardware
(WT)

LEDC_OVF_NUM_CHn Configures the maximum times of overflow minus 1. The LEDC_OVF_CNT_CHn_INT interrupt will be triggered when channel n overflows for (LEDC_OVF_NUM_CHn + 1) times. (R/W)

LEDC_OVF_CNT_EN_CHn Configures whether to enable the ovf_cnt of channel n.
0: Disable
1: Enable
(R/W)
```
Continued on the next page...
```