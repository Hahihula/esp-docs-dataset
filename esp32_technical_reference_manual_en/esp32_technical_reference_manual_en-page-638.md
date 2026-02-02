**Chapter Title:**
Chapter 28 LED PWM Controller (LEDC)

**Section Titles and Descriptions:**

1. **Register 28.3, LEDC_HSCHn_DUTY_REG (n: 0-7) (0x8+0x14*n):**
   - Description:
     ```
     LEDC_DUTY_HSCHn The register is used to control output duty. When hstimer(x=0[3]), selected by high-speed channel n, has reached LEDC_LPOINT_HSCHn, the output signal changes to low.
     (R/W)
     LEDC_LPOINT_HSCHn = LEDC_LPOINT_HSCHn[19:0] + LEDC_DUTY_HSCHn[24:4]
     LEDC_LPOINT_HSCHn = LEDC_LPOINT_HSCHn[19:0] + LEDC_DUTY_HSCHn[24:4] + 1
     ```
   - Reference to Functional Description for more information on when (1) or (2) is chosen.

2. **Register 28.4, LEDC_HSCHn_CONF1_REG (n: 0-7) (0xC+0x14*n):**
   - Descriptions:
     ```
     LEDC_DUTY_START_HSCHn When LEDC_DUTY_NUM_HSCHn, LEDC_DUTY_CYCLE_HSCHn and LEDC_DUTY_SCALE_HSCHn has been configured, these register will not take effect until LEDC_DUTY_START_HSCHn is set. This bit is automatically cleared by hardware.
     (R/W)
     
     LEDC_DUTY_INC_HSCHn This register is used to increase or decrease the duty of output signal for high-speed channel n.
     (R/W)
     
     LEDC_DUTY_NUM_HSCHn This register is used to control the number of times the duty cycle is increased or decreased for high-speed channel n. 
     (R/W)
     
     LEDC_DUTY_CYCLE_HSCHn This register is used to increase or decrease the duty cycle every time LEDC_DUTY_CYCLE_HSCHn cycles for high-speed channel n.
     (R/W)
     
     LEDC_DUTY_SCALE_HSCHn This register is used to increase or decrease the step scale for high-speed channel n. 
     (R/W)
     ```

**Footer:**
- Page number 638
- Document version ESP32 TRM (Version 5.6)

**Navigation Links at Bottom of Page:**  
- Submit Documentation Feedback

**Company Information in Footer:**
- Espressif Systems