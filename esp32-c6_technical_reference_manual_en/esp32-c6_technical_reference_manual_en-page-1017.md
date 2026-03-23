

```markdown
| PCNT_CHO_NEG_MODE_Un | PCNT_CHO_HCTRL_MODE_Un | Counter Mode |
|----------------------|------------------------|--------------|
|                      |                        |              |
| 1                    | 0                      | Increment    |
|                      | 1                      | Decrement    |
| Others               | Others                 | Disable      |
| 2                    | 0                      | Decrement    |
|                      | 1                      | Increment    |
| Others               | Others                 | Disable      |
| Others               | N/A                    | Disable      |

- Maximum count value: When pulse_cnt reaches PCNT_CNT_H_LIM_Un, a high limit interrupt is triggered and PCNT_CNT_THR_H_LIM_LAT_Un is high.
- Minimum count value: When pulse_cnt reaches PCNT_CNT_L_LIM_Un, a low limit interrupt is triggered and PCNT_CNT_THR_L_LIM_LAT_Un is high.
- Two threshold values: When pulse_cnt equals either PCNT_CNT_THRESO_Un or PCNT_CNT_THRESH1_Un, an interrupt is triggered and either PCNT_CNT_THRESO_LAT_Un or PCNT_CNT_THRES1_LAT_Un is high respectively.
- Zero: When pulse_cnt is 0, an interrupt is triggered and PCNT_CNT_THR_ZERO_LAT_Un is valid.

If PCNT_CNT_H_LIM_Un and/or PCNT_CNT_L_LIM_Un are reconfigured by software when PCNT is working, the new configuration will take effect after pulse_cnt counts to any of the above five watchpoints; If PCNT_CNT_THRESO_Un and/or PCNT_CNT_THRES1_Un are reconfigured by software, the new configuration will take effect immediately.
```

## 31.3 Applications

In each unit, channel 0 and channel 1 can be configured to work independently or together. The three subsections below provide details of channel 0 incrementing independently, channel 0 decrementing independently, and channel 0 and channel 1 incrementing together. For other working modes not elaborated in this section (e.g. channel 1 incrementing/decrementing independently, or one channel incrementing while the other decrementing), reference can be made to these three subsections.
```