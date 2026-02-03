**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Body Text:**

When the PWM timer is running, it generates the following timing events periodically and automatically:

- **UTEP**: The timing event generated when the PWM timer’s value equals to the value of the period field (`MCPWM_TIMERx_PERIOD`) and when the PWM timer is increasing.
  
- **UTEZ**: The timing event generated when the PWM timer’s value equals to zero and when the PWM timer is increasing.

- **DTEP**: The timing event generated when the PWM timer's value equals to the value of the period field (`MCPWM_TIMERx_PERIOD`) and when the PWM timer is decreasing.
  
- **DTEZ**: The timing event generated when the PWM timer’s value equals zero and when the PWM timer is decreasing.

**Figure Caption:**
Figures 36.3-10 to 36.3-12 show the timing waveforms of U/DTEP and U/DTEZ.

**Diagram Description (from Figure 36.3-10):**

The diagram shows a PWM timer with labeled steps from `0` through `6`. The labels indicate different states or events related to the PWM timer, such as "UTEP", "UTEZ", etc., corresponding to specific points on the waveform.

**Figure Caption for Diagram:**
Figure 36.3-10. UTEP and UTEZ Generation in Count-Up Mode

**Footer Information:**

Espressif Systems
ESP32-S3 TRM (Version 1.7)
Page number: 1335
Submit Documentation Feedback