**Chapter Title:**
Chapter 35 LED PWM Controller (LEDC)

**Body Text:**

For a particular PWM generator (PWMn), its Hpointn is sampled from the LEDEC_HPOINT_CHn field each time the selected timer’s counter overflows. Likewise, Lpointn is also sampled on every counter overflow and is calculated from the sum of the LEDEC_DUTY_CHn[18:4] and LEDEC_HPOINT_CHn fields. By setting Hpointn and Lpointn via the LEDEC_HPOINT_CHn and LEDEC_DUTY_CHn[18:4] fields, the relative phase and duty cycle of the PWM output can be set.

The PWM output signal (sig_outn) is enabled by setting LEDEC_SUG_OUT_EN_CHn. When LEDEC_SIG_OUT_EN_CHn is cleared, PWM signal output is disabled, and the output signal (sig_outn) will output a constant level as specified by LEDEC_IDLE_LV_CHn.

The bits LEDEC_DUTY_CHn[3:0] are used to either alter duty cycles of the PWM output signal (sig_outn) periodically or set them non-zero. When LEDEC_DUTY_CHn[3:0] is zero, then for every 16 cycles of sig_outn, LEDEC_DUTY_CHn[3:0] will have those PWM pulses that are one timer tick longer than the other (16- LEDEC_DUTY_CHn[3:0]) cycles. For instance, if LEDEC_DUTY_CHn[18:4] is set to 10 and LEDEC_DUTY_CHn[3:0] is set to 5, then 5 of 16 cycles will have a PWM pulse with duty value of 11 and the rest of the 16 cycles will have a PWM pulse with a duty value of 10. The average duty cycle after 16 cycles is 10.3125.

If fields LEDEC_TIMER_SEL_CHn, LEDEC_HPOINT_CHn, LEDEC_DUTY_CHn[18:4] and LEDEC_SUG_OUT_EN_CHn are reconfigured, LEDEC_PARA_UP_CHn must be set to apply the new configuration. This will cause the newly configured values to take effect upon the next overflow of the counter. LEDEC_PARA_UP_CHn field will be automatically cleared by hardware.

**Subsection Title:**
35.3.4 Duty Cycle Fading

The PWM generators can fade the duty cycle of a PWM output signal (i.e., gradually change the duty cycle from one value to another). If Duty Cycle Fading is enabled, the value of Lpointn will be incremented/decremented after a fixed number of counter overflows occurs.

**Figure Description:**
Figure 35.3-4 illustrates Duty Cycle Fading.
- The figure shows three different states (a, b, c) with corresponding duty cycles and cycle counts for LEDC_DUTY_CYCLE_CHn[18:0] in a PWM controller context:
  - State 'a': Lpointn is at the beginning of an increment/decrement sequence. 
  - State 'b': The counter has incremented or decremented to its new value.
  - State 'c': Another cycle count, showing progression through different duty cycles.

**Figure Caption:**
Figure 35.3-4 Output Signal Diagram of Fading Duty Cycle

**Additional Information on Duty Cycle Fading Configuration Using Register Fields:**

LEDEC_DUTY_CHn is used to set the initial value of Lpointn.
LEDEC_DUTY_START_CHn will enable/disable duty cycle fading when set/cleared.

LEDEC_DUTY_CYCLE_CHn sets the number of counter overflow cycles for every Lpointn increment/decrement. In other words, Lpointn will be incremented/decremented after LEDEC_DUTY_CYCLE_CHn counter overflows.
LEDEC_DUTY_INC_CHn configures whether Lpointn is incremented/decremented if set/cleared.

**Footer:**
Espressif Systems
1315 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback