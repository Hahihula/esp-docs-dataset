**Chapter Title:**
Chapter 38 Pulse Count Controller (PCNT)

**Body Text:**

- Independently filter glitches of input pulse signals (sig_ch0_un and sig_ch1_un) and control signals (ctrl_ch0_un and ctrl_ch1_un) on each unit

- Each channel has the following parameters:
  1. Selection between counting on positive or negative edges of the input pulse signal
  2. Configuration to Increment, Decrement, or Disable counter mode for control signal’s high and low states

- Maximum frequency of pulses: 40 MHz

**Subsection Title (in red):**
38.2 Functional Description

**Diagram Labels in Subsection:**

- ch0:
  - PCNT_FILTER_EN_Un
  - PCNT_CKHO_NEG_MODE_Un
  - PCNT_CKHO_POS_MODE_Un
  - pulse_cnt
  - ctrl_ch0_un
  - filter
  - inc_dec
  - comparator
  - PCNT_CNT_H_LIM_Un
  - PCNT_THR_H_LIM_EN
- ch1:
  - PCNT_FILTER_EN_Un
  - PCNT_CKHI_NEG_MODE_Un
  - PCNT_CKHI_POS_MODE_Un
  - pulse_cnt
  - ctrl_ch1_un
  - filter
  - inc_dec
  - comparator
  - PCNT_CNT_L_LIM_Un
  - PCNT_THR_L_LIM_EN

**Diagram Title:**
Figure 38.2-1. PCNT Unit Architecture

**Caption for Diagrams (in black text):**

Figure 38.2-1 shows PCNT’s architecture. As stated above, ctrl_ch0_un is the control signal for ch0 of unit n. Its high and low states can be assigned different counter modes and used for pulse counting of the channel’s input pulse signal sig_ch0_un on negative or positive edges.

**List under Caption:**

- Increment mode:
  - When a channel detects an active edge of sig_ch0_un (can be configured by software), the counter value pulse_cnt increases by 1. Upon reaching PCNT_CNT_H_LIM_Un, pulse_cnt is cleared.
  - If the channel’s counter mode is changed or if PCNT_CNT_PAUSE_Un is set before pulse_cnt reaches PCNT_CNT_H_LIM_Un, then pulse_cnt freezes and its counter mode changes.

**Footer:**
Espressif Systems
1441 ESP32-S3 TRM (Version 1.7)