**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Back Link:**
GoBack

**Register Information:**
- **Register Name:** MCPWM_GENO FORCE REG (0x04C)
- **Bit Positions and Values in Binary:**
  - Bit positions range from bit1 to bit5.
  - Each position is associated with a specific function:
    - bit1, set to TEP
    - bit2, set to TEA
    - bit3, set to TEB
    - bit4, set to sync (TEA/B below and here means an event generated when the timer's value equals that of register A/B)
    - bit5

**Description:**
- **MCPWM_GENO_CNTUFORCE_UPMETHOD:** Updating method for continuous software force of PWM generator0. When all bits are set to 0, immediately; when bit0 is set to 1 (TEZ); when bit1 is set to 1 (TEP); when bit2 is set to 1 (TEA); when bit3 is set to 1 (TEB); when bit4 is set to sync.
- **MCPWM_GENO_A_CNTUFORCE_MODE:** Continuous software force mode for PWMOA. Values: disabled, low, high; disabled.

**Additional Modes and Functions:**
- **MCPWM_GENO_B_CNTUFORCE_MODE:** Continuous software force mode for PWOBO. Values: disabled.
- **MCPWM_GENO_A_NCIFORCE:** Trigger of non-continuous immediate software-force event for PWMOA (toggle to trigger a force event).
- **MCPWM_GENO_A_NCIFORCE_MODE:** Non-continuous immediate software force mode for PWMOA with values 0: disabled, low; high.
- **MCPWM_GENO_B_NCIFORCE:** Trigger of non-continuous immediate software-force event for PWOBO (toggle to trigger a force event).
- **MCPWM_GENO_B_NCIFORCE_MODE:** Non-continuous immediate software force mode for PWMOB with values 0: disabled, low; high.

**Footer Information:**
- Page number and document version:
  - "1376 ESP32-S3 TRM (Version 1.7)"
- Company name at the bottom left corner.
- Link to submit documentation feedback on the right side of page footer:

(Note: The image contains a diagram with binary values, but it is not described in detail as per your instructions.)