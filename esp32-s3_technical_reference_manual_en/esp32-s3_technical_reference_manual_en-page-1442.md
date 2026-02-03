**Chapter Title:**
Chapter 38 Pulse Count Controller (PCNT)

**Tables and Descriptions:**

1. **Table 38.2-1:** Counter Mode, Positive Edge of Input Pulse Signal. Control Signal in Low State

   | PCNT_CHO_POS_MODE_Un | PCNT_CHO_LCTRL_MODE_Un | Counter Mode |
   |-----------------------|--------------------------|--------------|
   | 0                     | Increment                |             |
   | 1                     | Decrement                 |             |
   | Others                | Disable                   |             |

2. **Table 38.2-2:** Counter Mode, Positive Edge of Input Pulse Signal. Control Signal in High State

   | PCNT_CHO_POS_MODE_Un | PCNT_CHO_HCTRL_MODE_Un | Counter Mode |
   |-----------------------|-------------------------|--------------|
   | 0                     | Increment               |             |
   | 1                     | Decrement                |             |
   | Others                | Disable                  |             |

3. **Table 38.2-3:** Counter Mode, Negative Edge of Input Pulse Signal. Control Signal in Low State

   | PCNT_CHO_NEG_MODE_Un | PCNT_CHO_LCTRL_MODE_Un | Counter Mode |
   |-----------------------|-------------------------|--------------|
   | 0                     | Increment               |             |
   | 1                     | Decrement                |             |
   | Others                | Disable                  |             |

**Text Explanation:**

- **Decrement mode:** When a channel detects an active edge of sig_ch0_un (can be configured by software), the counter value pulse_cnt decreases by 1. Upon reaching PCNT_CNT_L_LIMIT_Un, pulse_cnt is cleared.
- If the channel's counter mode is changed or if PCNT_CNT_PAUSE_Un is set before pulse_cnt reaches PCNT_CNT_H_LIMIT_Un, then pulse_cnt freezes and its counter mode changes.

- **Disable mode:** Counting is disabled, and the counter value pulse_cnt freezes. 

**Additional Information:**

Each unit has one filter for all its control and input pulse signals. A filter can be enabled with the bit PCNT_FILTER_EN_Un.
The filter monitors the signals and ignores all the noise (i.e., the glitches with pulse widths shorter than PCNT_FILTER_THRESH_Un APB clock cycles in length).

As previously mentioned, each unit has two channels which process different input pulse signals and increase or decrease values via their respective inc_dec modules; then these channel sends these values to the

**Table 38.2-1 to Table 38.2-4:** provide information on how to configure the counter mode for channel O.

Espressif Systems
ESP32-S3 TRM (Version 1.7)