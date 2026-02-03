**Chapter Title:**
Chapter 38 Pulse Count Controller (PCNT)

**Table Title and Content:**
- **Title:** Table 38.2-4. Counter Mode. Negative Edge of Input Pulse Signal. Control Signal in High State

| PCNT_CHO_NEG_MODE_Un | PCNT_CHO_HCTRL_MODE_Un | Counter Mode |
|-----------------------|--------------------------|--------------|
|                      |                         | Increment    |
| 1                     | 0                        | Decrement    |
|                      | Others                   | Disable      |
| 2                     | 0                        | Decrement    |
|                      | Others                   | Increment    |
|                      | N/A                      | Disable      |

**Body Text:**
The PCNT has five watchpoints that share one interrupt. The interrupt can be enabled or disabled by interrupt enable signals of each individual watchpoint.

- **Maximum count value:** When pulse_cnt reaches `PCNT_CNT_H_LIM_Un`, a high limit interrupt is triggered and `PCNT_CNT_THR_H_LIM LAT_Un` is high.
  
- **Minimum count value:** When pulse_cnt reaches `PCNT_CNT_L_LIM_Un`, a low limit interrupt is triggered and `PCNT_CNT_THR_L_LIM LAT_Un` is high.

- Two threshold values: When pulse_cnt equals either `PCNT_CNT_THRESHOLDUn` or `PCNT_CNT_THRESHOLD1Un`, an interrupt is triggered, and either `PCNT_CNT_THR_THRESHOLD0Un` or `PCNT_CNT_THR_THRESHOLD1LAT_Un` is high respectively.
  
- **Zero:** When `pulse_cnt` is 0, an interrupt is triggered when both `PCNT_CNT_THR ZERO LAT_Un` are valid.

**Subsection Title:**
38.3 Applications

**Body Text (continued):**
In each unit, channel 0 and channel 1 can be configured to work independently or together. The three subsections below provide details of channel 0 incrementing independently, channel O decrementing independently, and channel 0 and channel 1 incrementing together.

For other working modes not elaborated in this section (e.g., channel 1 incrementing/decrementing independently), refer to these three subsections for more information. 

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Page Number:** 
1443