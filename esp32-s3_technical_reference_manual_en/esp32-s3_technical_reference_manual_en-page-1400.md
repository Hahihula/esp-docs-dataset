**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
Register 36.57. MCPWM_FH2_CFG1_REG (0x00DC)

**Table Description for Register 36.57:**
- **Columns:** Bits of the register
- **Rows:** Each bit is labeled with its corresponding name and function.
  - `MCPWM_FH2CLR_OST`: A rising edge will clear on going one-shot mode action (R/W)
  - `MCPWM_FHCBCPULSE`: Cycle-by-cycle mode action refresh moment selection. When bit0 is set to 1: TEZ; when bit1 is set to 1: TEP. (R/W)
  - `MCPWM_FH2FORCE_CBO`: A toggle triggers a cycle-by-cycle mode action. (R/W)
  - `MCPWM_FH2FORCE_OST`: A toggle (software negate its value) triggers a one-shot mode action.
    - Note: This is marked as read/write.

**Section Header:**
Register 36.58. MCPWM_FAULT_DETECT_REG (0x00E4)

**Table Description for Register 36.58:**
- **Columns:** Bits of the register
- **Rows:** Each bit is labeled with its corresponding name and function.
  - `MCPWM_FO_EN`: When set, event_f0 generation is enabled. (R/W)
  - `MCPWM_F1_EN`: When set, event_f1 generation is enabled. (R/W)
  - `MCPWM_F2_EN`: When set, event_f2 generation is enabled. (R/W)
  - `MCPWM_FO_POLE`: Set f0 trigger polarity on FAULT0 source from GPIO matrix; O: level low.
    - Note: This can be either "level high" or marked as read/write
  - `MCPWM_F1_POLE`: Set event_f1 trigger polarity on FAULT1 source from GPIO matrix. O: level low, 1: level high (R/W)
  - `MCPWM_F2_POLE`: Set event_f2 trigger polarity on FAULT2 source from GPIO matrix; O: level low.
    - Note: This can be either "level high" or marked as read/write
  - `MCPWM_EVENT_FO`: Set and reset by hardware. If set, event_f0 is ongoing (RO)
  - `MCPWM_EVENT_F1`: Set and reset by hardware. If set, event_f1 is on going.
    - Note: This can be either "going" or marked as read-only
  - `MCPWM_EVENT_F2`: Set and reset by hardware. If set, event_f2 is ongoing (RO)

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)