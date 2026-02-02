**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Back to Top Button:**
GoBack

**Register Information for Register 29.37, PWM_DT1_CFG_REG (0x0090):**

- **Field Descriptions and Values in Binary Format:** 
  - The binary format is displayed with each bit labeled from rightmost side.
  
- **Field Details Table:**
  - **PWM_DT1_CLK_SEL**: Dead time generator clock selection. Options are:
    - 0: PWM_clk
    - 1: PT_clk (R/W)
  - **PWM_DT1_B_OUTBYPASS, S0 in Table 29.3-5:** 
    - Read/Write access.
  - **PWM_DT1_A_OUTBYPASS, S1 in Table 29.3-5:** 
    - Read/Write access.

- **Additional Fields:**
  - **PWM_DT1_FED_OUTINVERT**: Options are:
    - R/W
  - **PWM_DT1_RED_OUTINVERT**: Option is (R/W)
  - **PWM_DT1_FED_INSEL, S5 in Table 29.3-5:** 
    - Read/Write access.
  - **PWM_DT1_RED_INSEL, S4 in Table 29.3-5:** 
    - Read/Write access.

- **Other Fields:**
  - **PWM_DT1_B_OUTSWAP**: Option is (R/W)
  - **PWM_DT1_A_OUTSWAP**: Option is (R/W)

- **Special Modes and Functions for PWM_DT1_DEB_MODE, S8 in Table 29.3-5:** 
  - Dual-edge B mode.
    - Options:
      - FED/RED take effect on different paths separately: R/W
      - FED (falling edge delay)/RED (rising edge delay) takes effect on the B path.

**Register Information for Register 29.38, PWM_DT1_FED_CFG_REG (0x0094):**

- **Field Descriptions and Values in Binary Format:** 
  - The binary format is displayed with each bit labeled from rightmost side.
  
- **Field Details Table:**
  - **PWM_DT1_RED_UPMETH**: Updating method for RED active register. Options are:
    - R/W
  - **PWM_DT1_FED_UPMETH**: Updating method for FED active register. Options include immediate updates based on bit0, bit1 to bit3 settings.

**Footer:**
Espressif Systems  
701 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback