**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack**

**Section Header:**
Register 36.44. MCPWM_FH2_STATUS_REG (0x0E0)

**Binary Representation and Description of Register:**
- Binary representation shown with bits labeled from right to left.
- Description:
  - `MCPWM_FH2_CBC_ON` Set and reset by hardware. If set, a cycle-by-cycle mode action is ongoing. (RO)
  - `MCPWM_FH2_OST_ON` Set and reset by hardware. If set, an one-shot mode action is on-going. (RO)

**Section Header:**
Register 36.45. MCPWM_GEN2_STMP_CFG_REG (0x0OAC)

**Binary Representation and Description of Register:**

- Binary representation shown with bits labeled from right to left.
- Description:
  - `MCPWM_GEN2_A_UPMETHOD` Update method for PWM generator 2 time stamp A’s active register. When all bits are set to O: immediately; when bit0 is set to 1: TEZ; when bit1 is set to 1: TEP; when bit2 is set to 1: sync; when bit3 is set to 1: disable the update. (R/W)
  - `MCPWM_GEN2_B_UPMETHOD` Update method for PWM generator 2 time stamp B’s active register. When all bits are set to O: immediately; when bit0 is set to 1: TEZ; when bit1 is set to 1: TEP; when bit2 is set to 1: sync; when bit3 is set to 1: disable the update. (R/W)
  - `MCPWM_GEN2_A_SHDW_FULL` Set and reset by hardware. If set, PWM generator 2 time stamp A’s shadow reg is filled and waiting to be transferred to A’s active reg. If cleared, A’s active reg has been updated with shadow register latest value. (R/WTC/SC)
  - `MCPWM_GEN2_B_SHDW_FULL` Set and reset by hardware. If set, PWM generator 2 time stamp B’s shadow reg is filled and waiting to be transferred to B’s active reg. If cleared, B’s active reg has been updated with shadow register latest value. (R/WTC/SC)

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)