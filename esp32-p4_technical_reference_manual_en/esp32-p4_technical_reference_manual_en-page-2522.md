

```markdown
Table 48.4-4. Counter Mode. Falling Edge of Input Pulse Signal. Control Signal in High State

| PCNT_CHO_NEG_MODE_Un | PCNT_CHO_HCTRL_MODE_Un | Counter Mode |
|----------------------|------------------------|--------------|
|                      |                        |              |
| 1                    | 0                      | Increment    |
|                      | 1                      | Decrement    |
|                      | Others                 | Disable      |
| 2                    | 0                      | Decrement    |
|                      | 1                      | Increment    |
|                      | Others                 | Disable      |
| Others               | N/A                    | Disable      |

Each unit has one filter for all its control and input pulse signals. A filter can be enabled by setting the bit PCNT_FILTER_EN_Un. The filter monitors the signals and ignores all the noise, i.e., the glitches with pulse widths shorter than PCNT_FILTER_THRES_Un APB clock cycles in length.

As shown on Figure 48.3-1, each unit has two channels which process different input pulse signals and increase or decrease values via their respective inc_dec modules, then the two channels send these values to the counter module which has a 16-bit wide signed register. This counter can be suspended by setting PCNT_CNT_PAUSE_Un, and cleared by setting PCNT_PULSE_CNT_RST_Un.

The PCNT has five watchpoints that share one interrupt. The interrupt can be enabled or disabled by interrupt enable signals of each individual watchpoint.

* Maximum count value: When pulse_cnt reaches PCNT_CNT_H_LIM_Un, a high limit interrupt is triggered and PCNT_CNT_THR_H_LIM_LAT_Un is high.
* Minimum count value: When pulse_cnt reaches PCNT_CNT_L_LIM_Un, a low limit interrupt is triggered and PCNT_CNT_THR_L_LIM_LAT_Un is high.
* Two threshold values: When pulse_cnt equals either PCNT_CNT_THRES0_Un or PCNT_CNT_THRES1_Un, an interrupt is triggered and either PCNT_CNT_THR_THRES0_LAT_Un or PCNT_CNT_THR_THRES1_LAT_Un is high respectively.
* Zero: When pulse_cnt is 0, an interrupt is triggered and PCNT_CNT_THR_ZERO_LAT_Un is valid.

If PCNT_CNT_H_LIM_Un and/or PCNT_CNT_L_LIM_Un are reconfigured by software when PCNT is working, the new configuration will take effect after pulse_cnt counts to any of the above five watchpoints; If PCNT_CNT_THRES0_Un and/or PCNT_CNT_THRES1_Un are reconfigured by software, the new configuration will take effect immediately.

## 48.5 Interrupts

ESP32-P4's PCNT can generate the following interrupt signal that will be sent to the Interrupt Matrix.
* **PCNT_INT**

There are several internal interrupt sources from PCNT that can generate the above interrupt signal. The interrupt sources from PCNT are listed with their trigger conditions and the resulted interrupt signal in Table 48.5-1.
```