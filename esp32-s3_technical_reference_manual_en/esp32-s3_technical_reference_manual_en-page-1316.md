**Chapter Title:**
Chapter 35 LED PWM Controller (LEDC)

**Body Text with List Items and Descriptions:**

- **LED_CUTY_SCALE_CHn**: Sets the amount that Lpointn is incremented/decremented.
  
- **LED_CUTY_NUM_CHn**: Sets the maximum number of increments/decrements before duty cycle fading stops.

If the fields LEDC_DUTY_CHn, LEDC_DUTY_START_CHn, LEDC_DUTY_CYCLE_CHn, LEDC_DUTY_INC_CHn,
LED_CUTY_SCALE_CHn, and LEDC_DUTY_NUM_CHn are reconfigured, LEDC PARA UP CHn must be set to apply the new configuration. After this field is set, the values for duty cycle fading will take effect at once.
LEDC PARA UP CHn field will be automatically cleared by hardware.

**Subsection Title:**
35.3.5 Interrupts

- **LED_CUTY_CNT_CHn_INT**: Triggered when the timer counter overflows (LED_CUTY_NUM_CHn + 1) times and the register LED_CUTY_CNT_EN_CHn is set to 1.
  
- **LED_CUTY_CHNG_END_CHn_INT**: Triggered when a fade on an LED PWM generator has finished.

- **LED TIMERx OVF_INT**: Triggered when an LED PWM timer has reached its maximum counter value. 

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Information:**
ESP32-S3 TRM (Version 1.7)