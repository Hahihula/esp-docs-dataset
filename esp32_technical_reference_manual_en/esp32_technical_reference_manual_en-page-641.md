**Chapter Title:**
Chapter 28 LED PWM Controller (LEDC)

**Section Header:**
GoBack

**Register Information for Register 28.9, LEDC_LSCHn_CONF1_REG**

- **Description:** 
  - `LEDC_DUTY_START_LSCHn`: When `LEDC_DUTY_NUM_HSCHn`, `LEDC_DUTY_CYCLE_HSCHn` and `LEDC_DUTY_SCALE_HSCHn` have been configured, these settings will not take effect until set.
  - `LEDC_DUTY_START_HSCHn`: This bit is automatically cleared by hardware. (R/W)
- **Hexadecimal Values:**
  - `0x000`
  - `0x000`

**Register Information for Register 28.10, LEDC_LSCHn_DUTY_R_REG**

- **Description:** 
  - This register represents the current duty of the output signal for low-speed channel n.
- **Hexadecimal Values:**
  - `0x00`
  - `0x0000000`

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version:** 
641 ESP32 TRM (Version 5.6)