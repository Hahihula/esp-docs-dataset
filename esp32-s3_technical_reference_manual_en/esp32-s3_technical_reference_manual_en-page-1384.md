**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Subtitle:**
Register 36.33. MCPWM_GEN1_CFG0_REG (0x080)

**Binary Register Diagram Description:**
- The diagram shows a binary register with bits labeled from '31' to '0'.
- Each bit is represented by either an 'X' or the number of its position.
- There are labels for specific fields such as "MCPWM_GEN1_T1_SEL" and others, but they appear in redacted form.

**Text Descriptions:**

1. **MCPWM_GEN1_CFG_UPMETHOD**
   - Description:
     ```
     Update method for PWM generator 1's active register of configuration.
     When all bits are set to O: immediately; when bit0 is set to 1: TEZ;
     when bit1 is set to 1:sync; when bit3 is set to 1:disable the update. (R/W)
     ```

2. **MCPWM_GEN1_TO_SEL**
   - Description:
     ```
     Source selection for PWM generator 1 event_t0, take effect immediately,
     O: fault_event0, 1: fault_event1, 2: fault_event2, 3: sync_taken, 4: none. (R/W)
     ```

3. **MCPWM_GEN1_T1_SEL**
   - Description:
     ```
     Source selection for PWM generator 1 event_t1, take effect immediately,
     O: fault_event0, 1: fault_event1, 2: fault_event2, 3: sync_taken, 4: none. (R/W)
     ```

**Footer Information:**
- "Espressif Systems"
- Page number and document version:
  ```
  ESP32-S3 TRM (Version 1.7)
  ```