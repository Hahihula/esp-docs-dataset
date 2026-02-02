**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

---

**Register Section:**

- **Register Name and Address:**
  - Register 29.17. PWM_GENO_TSTMP_A_REG (0x040)
    - Description: (reserved)
    - Bit Map:
      ```
      31   16   15
      0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
      Reset
      PWM_GENO_A PWM generator O time stamp A’s shadow register. (R/W)
      ```

- **Register Name and Address:**
  - Register 29.18. PWM_GENO_TSTMP_B_REG (0x044)
    - Description: (reserved)
    - Bit Map:
      ```
      31   16   15
      0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
      Reset
      PWM_GENO_B PWM generator O time stamp B’s shadow register. (R/W)
      ```

- **Register Name and Address:**
  - Register 29.19. PWM_GENO_CFGO_REG (0x048)
    - Description:
      ```
      Bit Map:
        31   10   9   7   6   4   3   0
        0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
      Reset

      PWM_GENO_T1_SEL Source selection for PWM generator O event_t1, taking effect immediately. 
          - 0: fault_event0; 1: fault_event1; 2: fault_event2; 3: sync_taken; 4: none.
      (R/W)

      PWM_GENO_TO_SEL Source selection for PWM generator O event_t0, taking effect immediately,
          - 0: fault_event0; 1: fault_event1; 2: fault_event2; 3: sync_taken; 4: none. 
      (R/W)

      PWM_GENO_CFG_UPMETHOD Updating method for PWM generator O’s active register of configuration.
          - When all bits are set to 0: immediately; when bit0 is set to 1: TEZ;
          - When bit1 is set to 1: TEP; when bit2 is set to 1: sync; when bit3 is set to 1: disable the update. 
      (R/W)
      ```

**Footer Information:**  
Espressif Systems  
688 ESP32 TRM (Version 5.6)  

**Action Links:**  
Submit Documentation Feedback