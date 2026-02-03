**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
Register 36.52. MCPWM_DT2_CFG_REG (0x00C8)

**Binary Register Diagram Description:**
The diagram shows a binary register with various fields labeled, such as "MCPWM_DT2_GCLK SEL," "MCPWM_DT2_OUTBYPASS," and others.

**Field Descriptions in Text Format:**

- **MCPWM_DT2_FED_UPMETHOD:** Update method for FED (falling edge delay) active register. 0: immediate; when bit0 is set to 1: tez; when bit1 is set to 1: tep; when bit2 is set to 1: sync; when bit3 is set to 1: disable the update. (R/W)
  
- **MCPWM_DT2_RED_UPMETHOD:** Update method for RED (rising edge delay) active register. 0: immediate; when bit0 is set to 1: tez; when bit1 is set to 1: tep; when bit2 is set to 1: sync; when bit3 is set to 1: disable the update. (R/W)
  
- **MCPWM_DT2_DEB_MODE:** S8 in table 36.3-5, dual-edge B mode. 0: fed/red take effect on different path separately; 1: fed/red take effect on both paths simultaneously.
  
- **MCPWM_DT2_A_OUTSWAP:** S6 in table 36.3-5 (R/W)
  
- **MCPWM_DT2_B_OUTSWAP:** S7 in table 36.3-5 (R/W)
  
- **MCPWM_DT2_RED_INSEL:** S4 in table 36.3-5 (R/W)
  
- **MCPWM_DT2_FED_INSEL:** S5 in table 36.3-5 (R/W)
  
- **MCPWM_DT2_RED_OUTINVERT:** S2 in table 36.3-5 (R/W)
  
- **MCPWM_DT2_FED_OUTINVERT:** S3 in table 36.3-5 (R/W)
  
- **MCPWM_DT2_A_OUTBYPASS:** S1 in table 36.3-5 (R/W)
  
- **MCPWM_DT2_B_OUTBYPASS:** S0 in table 36.3-5 (R/W)
  
- **MCPWM_DT2_CLK_SEL:** Dead time generator 2 clock selection. 0: PWM_clk, 1: PT_clk.

**Section Header:**
Register 36.53. MCPWM_DT2_FED_CFG_REG (0x00CC)

**Binary Register Diagram Description:**
The diagram shows a binary register with various fields labeled similarly to the previous one but without specific descriptions provided in text format for this section.
  
- **MCPWM_DT2_FED:** Shadow register for FED. (R/W) 

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback