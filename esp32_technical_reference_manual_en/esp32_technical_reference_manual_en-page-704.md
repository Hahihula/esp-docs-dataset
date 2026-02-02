**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
Register 29.42. PWM_FH1_CFG1_REG (0x00a4)

**Body Text with Table and Descriptions for Bits in Register 29.42:**

- **PWM_FH1 FORCE OST**: A toggle (software negation of this bit’s value) triggers a one-shot mode action.
  - Description: (R/W)
  
- **PWM_FH1 FORCE CBC**: A toggle triggers a cycle-by-cycle mode action selection when bit0 is set to TEZ; When bit1 is set to TEP. 
  - Description: (R/W)

- **PWM_FH1 CBCPULSE**: The cycle-by-cycle mode action refresh moment selection.
  - Description: Set to 1: TEZ, Clear on-going one-shot mode when bit0 is clear.

**Section Header:**
Register 29.43. PWM_FH1_STATUS_REG (0x00a8)

**Body Text with Table and Descriptions for Bits in Register 29.43:**

- **PWM_FH1 OST ON**: Set and reset by hardware.
  - Description: If set, a one-shot mode action is on-going.

- **PWM_FH1 CBC ON**: Set and reset by hardware.
  - Description: If set, a cycle-by-cycle mode action is ongoing. (RO)

**Footer Information:**
Espressif Systems
Page Number: 704
Document Title: ESP32 TRM (Version 5.6)
Link Texts:
- Submit Documentation Feedback