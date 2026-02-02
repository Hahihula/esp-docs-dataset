**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
Register 29.44. PWM_GEN2_STMP_CFG_REG (0x0ac)

**Table Description for Register 29.44:**
- **Field Name:** PWM_GEN2_B_SHOW_FULL
- **Description:** Set and reset by hardware.
- **Additional Information:** If set, PWM generator time stamp B's shadow register is filled and to be transferred to timestamp B's active register.

- **Field Name:** PWM_GEN2_A_SHOW_FULL
- **Description:** Set and reset by hardware. 
- **Additional Information:** If set, PWM generator time stamp A's shadow register is filled and to be transferred to timestamp A's active register.
  
- **Field Name:** PWM_GEN2_B_UPMETHO
- **Description:** Updating method for PWM generator 2 time stamp B’s active register.

- **Field Name:** PWM_GEN2_A_UPMETHO
- **Description:** Updating method for PWM generator 2 time stamp A's active register.
  
**Section Header:**
Register 29.45. PWM_GEN2_TSTMP_A_REG (0x00b0)

**Table Description for Register 29.45:**
- **Field Name:** PWM_GEN2_A
- **Description:** PWM generator time stamp A's shadow register.

**Section Header:**
Register 29.46. PWM_GEN2_TSTMP_B_REG (0x00b4)

**Table Description for Register 29.46:**
- **Field Name:** PWM_GEN2_B
- **Description:** PWM generator time stamp B's shadow register.

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

**Document Version and Type:**
ESP32 TRM (Version 5.6)