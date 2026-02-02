**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Register Information:**

- **Register Name:** PWM_DTO_CFG_REG (0x0058)
- **Register Address:** Not explicitly provided, but referenced in the text.

**Field Descriptions and Values for Register 29.23:**
- **PWM_DTO_CLK_SEL**: Dead time generator clock selection.
  - 0: PWM.clk
  - 1: PT.clk (R/W)
- **PWM_DTO_B_OUTBYPASS, PWM_DTO_A_OUTBYPASS**:
  - S0 in Table 29.3-5 (R/W) and R/W respectively for both.
- **PWM_DTO_FED_OUTINVERT**: 
  - SS1 in Table 29.3-5
- **PWM_DTO_RED_OUTINVERT, PWM_DTO_RED_INSEL**:
  - S2/S4/SS6 in Table 29.3-5 (R/W)
- **PWM_DTO_B_OUTSWAP**: 
  - SS7 in Table 29.3-5
- **PWM_DTO_A_OUTSWAP, PWM_DTO_DEB_MODE**:
  - S8/S9/SS10 in Table 29.3-5 (R/W)
- **PWM_DTO_RED_UPMETH**: 
  - Updating method for RED active register.
    - When bit0 is set to: TEZ; when bit1 is set to TEP; when bit2 is set to sync
    - When bit3 is set to disable the update. (R/W)
- **PWM_DTO_FED_UPMETH**:
  - Updating method for FED active register.
    - When bit0 is set: TEZ; when bit1 is set TEP; when bit2 is set to sync
    - When bit3 is set to disable the update. (R/W)

**Field Descriptions and Values for Register 29.24:**
- **PWM_DTO_FED_CFG_REG (0x005c)**:
  - PWM_DTO_FED**: Shadow register for FED.
    - R/W

**Footer Information:**
- Page number: 692
- Document version: ESP32 TRM (Version 5.6)
- Company name: Espressif Systems
- Links: Submit Documentation Feedback