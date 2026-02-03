**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Back Link:**
GoBack

**Register Information for MCPWM_GENO_STMP_CFG_REG (0x003C):**

- **Field Description:** 
  - `MCPWM_GENO_A_UPMETHOD`
    - **Description:** Update method for PWM generator O time stamp A’s active register.
      - When all bits are set to 0: immediately; when bit0 is set to 1: TEZ;
      - When bit2 is set to 1: sync; when bit3 is set to 1: disable the update. (R/W)
  
  - **Field Description:** 
    - `MCPWM_GENO_B_UPMETHOD`
      - Update method for PWM generator O time stamp B’s active register.
      - When all bits are set to 0: immediately; when bit0 is set to 1: TEZ;
      - When bit2 is set to 1: sync; when bit3 is set to 1: disable the update. (R/W)
  
  - **Field Description:** 
    - `MCPWM_GENO_A_SHDW_FULL`
      - Set and reset by hardware.
        - If set, PWM generator O time stamp A’s shadow reg is filled and waiting to be transferred to A’s active reg; if cleared, A’s active reg has been updated with shadow register latest value. (R/W/TSC)
  
  - **Field Description:** 
    - `MCPWM_GENO_B_SHDW_FULL`
      - Set and reset by hardware.
        - If set, PWM generator O time stamp B’s shadow reg is filled and waiting to be transferred to B’s active reg; if cleared, B’s active reg has been updated with shadow register latest value. (R/W/TSC)

**Register Information for MCPWM_GENO_STMP_A_REG (0x0040):**

- **Field Description:** 
  - `MCPWM_GENO_A_PWM`
    - PWM generator O time stamp A's shadow register.
      - Read/Write

**Footer:**
Espressif Systems
1374 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback