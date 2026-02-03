**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
Register 36.28. MCPWM_FHO_CFG1_REG (0x006C)

**Table Description for Register 36.28:**
- The table shows the bits of register 36.28 with labels and descriptions:
  - `MCPWM_FHOCLR_OST`: A rising edge will clear on going one-shot mode action.
  - `MCPWM_FCBCPULSE`: Cycle-by-cycle mode action refresh moment selection (set to 1: TEZ; when bit0 is set to 1: TEP.).
  - `MCPWM_FHOFORCE_CBC`: A toggle triggers a cycle-by-cycle mode action.
  - `MCPWM_FHOFORCE_OST`: A toggle (software negate its value) triggers a one-shot mode action.

**Section Header:**
Register 36.29. MCPWM_FHO_STATUS_REG (0x0070)

**Table Description for Register 36.29:**
- The table shows the bits of register 36.29 with labels and descriptions:
  - `MCPWM_FCBCON`: Set and reset by hardware.
  - If set, a cycle-by-cycle mode action is ongoing (set to RO).
  - `MCPWM_FHOOST_ON`: Set and reset by hardware.

**Footer:**
- Page number: 1382
- Document version information: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems
- Link text for feedback submission: Submit Documentation Feedback