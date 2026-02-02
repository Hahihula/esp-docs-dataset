**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

---

**Section Header:**
Register 29.64. PWM_CAP_CHO_REG (0x00fc)

- **Field Description:**
  - `PWM_CAP_CHO_REG`: Value of the last capture on channel 0.
  - Access Mode: Read Only
  - Reset Option Available
  
**Field Values and Reset Options:** 
- [31, 0] (Reset)
  
---

**Section Header:**
Register 29.65. PWM_CAP_CH1_REG (0x0100)

- **Field Description:**
  - `PWM_CAP_CH1_REG`: Value of the last capture on channel 1.
  - Access Mode: Read Only
  - Reset Option Available
  
**Field Values and Reset Options:** 
- [31, 0] (Reset)
  
---

**Section Header:**
Register 29.66. PWM_CAP_CH2_REG (0x0104)

- **Field Description:**
  - `PWM_CAP_CH2_REG`: Value of the last capture on channel 2.
  - Access Mode: Read Only
  - Reset Option Available
  
**Field Values and Reset Options:** 
- [31, 0] (Reset)
  
---

**Section Header:**
Register 29.67. PWM_CAP_STATUS_REG (0x0108)

- **Field Description:**
  - `PWM_CAP_STATUS_REG`: Various edge detection triggers on different channels.
    - `PWM_CAP2_EDGE`: Edge of the last capture trigger on channel 2, 0: posedge; 1: negedge. Access Mode Read Only
    - `PWM_CAP1_EDGE`: Edge of the last capture trigger on channel 1, 0: posedge; 1: negedge. Access Mode Read Only
    - `PWMCAPEO_EDGE`: Edge of the last capture trigger on channel 0, 0: posedge; 1: negedge. Access Mode Read Only
  
**Field Values and Reset Options:** 
- [31, (reserved), 2, 1, 0] (Reset)
  
---

**Footer Information:**
Espressif Systems
Page Number: 717
Document Version: ESP32 TRM (Version 5.6)

**Link for Feedback Submission:**
Submit Documentation Feedback