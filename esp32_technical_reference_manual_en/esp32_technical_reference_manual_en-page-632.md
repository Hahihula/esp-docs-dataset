**Chapter Title:**
Chapter 28 LED PWM Controller (LEDC)

**Body Text:**

By using these two values, the relative phase and the duty cycle of the PWM output can be set. Figure 28.2-4 illustrates this.

![Figure 28.2-4](image-link) **LED PWM Output Signal Diagram**
LEDC_DUTY_HSCHn is a fixed-point register with four fractional bits. As mentioned before, when LEDC_DUTY_ HSCHn[24..4] is used in the PWM calculation directly, LEDC_DUTY_HSCHn[3..0] can be used to dither the output. If this value is non-zero, with a statistical chance of LEDC_DUTY_HSCHn[3..0]/16, the actual PWM pulse will be one cycle longer. This effectively increases the resolution of the PWM generator to 25 bits, but at the cost of a slight jitter in the duty cycle.

The channels also have the ability to automatically fade from one duty cycle value to another. This feature is enabled by setting LEDC_DUTY_START_HSCHn. When this bit is set, the PWM controller will automatically increment or decrement the value in LEDC_DUTY_HSCHn, depending on whether the bit LEDC_DUTY_INC_HSCHn is set or cleared, respectively. The speed the duty cycle changes is defined as such: every time the LEDC_DUTY_CYCLE_ HSCHn cycles, the content of LEDC_DUTY_SCALE_HSCHn is added to or subtracted from LEDC_DUTY_HSCHn[24..4]. The length of the fade can be limited by setting LEDC_DUTY_NUM_HSCHn: the fade will only last that number of cycles before finishing. A finished fade also generates an interrupt.

![Figure 28.2-5](image-link) **Output Signal Diagram of Fading Duty Cycle**
Figure 28.2-5 is an illustration of this. In this configuration, LEDC_DUTY_NUM_HSCHn_R increases by LEDC_DUTY_SCALE_HSCHn for every LEDC_DUTY_CYCLE_HSCHn clock cycles, which is reflected in the duty cycle of the output signal.

**Notes:**
- When the LEDC is in fade mode, it is not supported to perform operations (e.g., pause) on the process or configure the following registers:
  - LEDC_HPOINT_H/LSCHn
  - LEDC_DUTY_H/LSCHn

**Footer Information:** 
Espressif Systems  
632  
ESP32 TRM (Version 5.6)

[Submit Documentation Feedback](link)