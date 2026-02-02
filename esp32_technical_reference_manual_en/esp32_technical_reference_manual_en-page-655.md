**Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Figure Captions and Descriptions:**

1. **Figure 29.3-8:** Count-Up/Down Mode Waveforms, Count-Down at Synchronization Event

   - The figure shows a waveform diagram with labels for "PWM Timer" values of `0xFFFFF` on the y-axis (indicating period setting) and `0x0000` indicating phase settings. There is also an axis labeled "Sync Input." A line graph illustrates waveforms over time.

2. **Figure 29.3-9:** Count-Up/Down Mode Waveforms, Count-Up at Synchronization Event

   - Similar to Figure 29.3-8 with the same y-axis labels and Sync Input label but showing a different waveform pattern indicating count-up events during synchronization.
   
**Body Text:**

When the PWM timer is running, it generates the following timing events periodically and automatically:

- **UTEP**
  The timing event generated when the PWM timer's value equals to the value of the period register (PWM_TIMER_X__PERIOD) and when the PWM timer is increasing.

- **UTEZ**
  The timing event generated when the PWM timer’s value equals zero and when the PWM timer is increasing.
  
- **DTEP**
  The timing event generated when the PWM timer's value equals to the value of the period register (PWM_TIMER_X__PERIOD) and when the PWM timer is decreasing.

- **DTEZ**
  The timing event generated when the PWM timer’s value equals zero and when the PWM timer is decreasing.

**Footer:**

Espressif Systems  
655  
ESP32 TRM (Version 5.6)

**Navigation Link:** Submit Documentation Feedback

**GoBack Button:** GoBack