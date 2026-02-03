**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

**Register Information:**
- **Register Name and Address:** MCPWM_TIMER2_CFG1_REG (0x028)
- **Bit Positions in Register:**
  - Bit positions are labeled from left to right as follows:
    ```
    31  | reserved
    5   |
    4   |
    3   |
    2   |
    1   |
    0   | Reset
    ```

**Section Title:** MCPWM_TIMER2_START

- **Description:**
  - "PWM timer2 start and stop control. (R/W/SC)"
  
- **Bit Values Explanation with Descriptions:**
  ```
  0: if PWM timer2 starts, then stops at TEZ;
  1: if timer2 starts, then stops at TEP;
  2: PWM timer2 starts and runs on;
  3: timer2 starts and stops at the next TEZ;
  4: timer2 starts and stops at the next TEP.
  
  TEP here and below means the event that happens when the timer equals to period."
  ```

**Section Title:** MCPWM_TIMER2_MOD

- **Description:**
  - "PWM timer2 working mode. (R/W)"
  
- **Bit Values Explanation with Descriptions:**
  ```
  0: freeze;
  1: increase mode;
  2: decrease mode;
  3: up-down mode.
  ```

**Footer Information:** 
- Company Name and Document Version:
  - "Espressif Systems"
  - "ESP32-S3 TRM (Version 1.7)"
  
- **Link for Submitting Documentation Feedback:**
  - "Submit Documentation Feedback"