**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Register Information for Register 36.37, MCPWM_DT1_CFG_REG (0x0090):**

- **Title:** Register 36.37. MCPWM_DT1_CFG_REG (0x0090)
  
- **Bit Description:**
  - `MCPWM_DT1_CLK_SEL` to `MCPWM_DT1_OUTBYPASS`: These bits are reserved.
  - `MCPWM_DT1_FED_UPMETHOD`: Update method for FED active register. 
    - When bit0 is set to 1, it means "tez".
    - When bit1 is set to 1, it means "tep".
    - When bit2 is set to 1, it means "sync".
    - When bit3 is set to 1: disable the update.
      (R/W)
  
- **Bit Description for MCPWM_DT1_RED_UPMETHOD:** 
  - Update method for RED active register. 
    - When bit0 is set to 1: tez
    - When bit1 is set to 1: tep
    - When bit2 is set to 1: sync
    - When bit3 is set to 1: disable the update.
      (R/W)
  
- **Bit Description for MCPWM_DT1_DEB_MODE:** 
  - S8 in table 36.3-5, dual-edge B mode:
    - O: fed/red take effect on different path separately; 1: fed/red take effect on both paths simultaneously
    - A out is in bypass or dulpB mode.
      (R/W)
  
- **Bit Description for MCPWM_DT1_A_OUTSWAP:** 
  - S6 in table 36.3-5:
    - Read/Write
  
- **Bit Description for MCPWM_DT1_B_OUTSWAP:** 
  - S7 in table 36.3-5: (R/W)
  
- **Bit Description for MCPWM_DT1_RED_INSEL:** 
  - S4 in table 36.3-5:
    - Read/Write
  
- **Bit Description for MCPWM_DT1_FED_INSEL:** 
  - S5 in table 36.3-5: (R/W)
  
- **Bit Description for MCPWM_DT1_RED_OUTINVERT:** 
  - S2 in table 36.3-5:
    - Read/Write
  
- **Bit Description for MCPWM_DT1_FED_OUTINVERT:** 
  - S3 in table 36.3-5: (R/W)
  
- **Bit Description for MCPWM_DT1_A_OUTBYPASS:** 
  - S1 in table 36.3-5:
    - Read/Write
  
- **Bit Description for MCPWM_DT1_B_OUTBYPASS:** 
  - SO in table 36.3-5: (R/W)
  
- **Bit Description for MCPWM_DT1_CLK_SEL:** Dead time generator clock selection.
  - O: PWM_clk, I: PT_clk:
    - Read/Write
  
**Register Information for Register 36.38, MCPWM_DT1_FED_CFG_REG (0x0094):**

- **Title:** Register 36.38. MCPWM_DT1_FED_CFG_REG (0x0094)
  
- **Bit Description:**
  - `MCPWM_DT1_FED`: Shadow register for FED.
    - Read/Write
  
**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)