**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
Register 36.23. MCPWM_DTO_CFG_REG (0x0058)

**Binary Diagram Description for Register 36.23:**
- The diagram shows a binary representation of the register with various fields labeled, such as "MCPWM_DTO_CLK_SEL" and others.
- Each bit position is numbered from left to right.

**Field Descriptions in Text Format (for MCPWM_DTO_CFG_REG):**

1. **MCPWM_DTO_FED_UPMETHOD**
   - Description: Update method for FED (rising edge delay) active register
   - Values:
     - 0: immediate; when bit0 is set to 1: tez;
     - When bit1 is set to 1: tep;
     - When bit2 is set to 1: sync;
     - When bit3 is set to 1: disable the update.
   - Access: Read/Write (R/W)

2. **MCPWM_DTO_RED_UPMETHOD**
   - Description: Update method for RED (rising edge delay) active register
   - Values:
     - 0: immediate; when bit0 is set to 1: tez;
     - When bit1 is set to 1: tep;
     - When bit2 is set to 1: sync;
     - When bit3 is set to 1: disable the update.
   - Access: Read/Write (R/W)

3. **MCPWM_DTO_DEB_MODE**
   - Description: S8 in table 36.3-5, dual-edge B mode
   - Values:
     - 0: fed/red take effect on different path separately; 
     - 1: fed/red take effect on both paths.
   - Access: Read/Write (R/W)

4. **MCPWM_DTO_A_OUTSWAP**
   - Description: S6 in table 36.3-5
   - Values:
     - R/W

5. **MCPWM_DTO_B_OUTSWAP**
   - Description: S7 in table 36.3-5 (R/W)

6. **MCPWM_DTO_RED_INSEL**
   - Description: S4 in table 36.3-5
   - Values:
     - R/W

7. **MCPWM_DTO_FED_INSEL**
   - Description: S5 in table 36.3-5 (R/W)

8. **MCPWM_DTO_RED_OUTINVERT**
   - Description: S2 in table 36.3-5
   - Values:
     - R/W

9. **MCPWM_DTO_FED_OUTINVERT**
   - Description: S3 in table 36.3-5 (R/W)

10. **MCPWM_DTO_A_OUTBYPASS**
    - Description: S1 in table 36.3-5
    - Values:
      - R/W

11. **MCPWM_DTO_B_OUTBYPASS**
    - Description: S0 in table 36.3-5 (R/W)

12. **MCPWM_DTO_CLK_SEL**
    - Description: Dead time generator O clock selection
    - Values:
      - P: PWM_clk, 
      - T: PT_clk.
    - Access: Read/Write (R/W)

**Section Header for Register 36.24:**
Register 36.24. MCPWM_DTO_FED_CFG_REG (0x005C)

**Binary Diagram Description for Register 36.24:**
- Similar to the previous register, this diagram shows a binary representation with various fields labeled.
- Each bit position is numbered from left to right.

**Field Descriptions in Text Format (for MCPWM_DTO_FED_CFG_REG):**

1. **MCPWM_DTO_FED**
   - Description: Shadow register for FED
   - Access: Read/Write (R/W)

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Submission Link Texts:
  - "Submit Documentation Feedback"