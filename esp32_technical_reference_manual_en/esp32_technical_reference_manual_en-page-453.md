**Chapter Title:**
Chapter 23 Pulse Count Controller (PCNT)

**Section Header:**
23.2.4 Examples

**Figure Caption and Description:**
- **Figure 23.2-2:** PULSE_CNT Upcounting Diagram.
  - Text below the figure explains that Figure 23.2-2 shows channel 0 being used as an up-counter, with a configuration example provided:
    - `CNT_CHO_POS_MODE_Un = 1`: Increase counter on the rising edge of sig_ch0_un
    - `PCNT_CHO_NEG_MODE_Un = 0`: No counting on the falling edge of sig_ch0_un.
    - `PCNT_CHO_LCTRL_MODE_Un = 0`: Do not modify counter mode when ctrl_ch0_un is low.
    - `PCNT_CHO_HCTRL_MODE_Un = 2`: Do not allow counter increments/decrements when ctrl_ch0_un is high.
    - `PCNT_CNT_H_LIM_Un = 5`: PULSE_CNT resets to 0 when the count value increases to 5.

- **Figure 23.2-3:** PULSE_CNT Downcounting Diagram
  - Text below this figure explains that Figure 23.2-3 shows channel 0 decrementing the counter, with a configuration example provided:
    - `PCNT_CHO_LCTRL_MODE_Un = 1`: Invert counter mode when ctrl_ch0_un is at low level; so it will decrease rather than increase.
    - `PCNT_CNT_H_LIM_Un = -5`: PULSE_CNT resets to 0 when the count value decreases to –5.

**Subsection Header:**
23.2.5 Interrupts

**Text Description for Subsection:**
- Text explains that PCNT_CNT_THR_EVENT_Un_INT: This interrupt gets triggered when one of the five channel comparators detects a match.
  
**Footer Information:**
Espressif Systems
453 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Navigation Link:**
GoBack