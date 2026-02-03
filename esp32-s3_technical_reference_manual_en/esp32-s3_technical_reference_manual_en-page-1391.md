**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

**Section Header:**
Register 36.42. MCPWM_FH1_CFG1_REG (0x00A4)

**Binary Representation Table for Register 36.42:**
- Binary bits are displayed in a table format with labels such as "MCPWM_FH1_FORCE_CBC", etc.
- The binary representation is shown from bit positions to the least significant bit.

**Description of Register 36.42 (MCPWM_FH1_CFG1_REG):**

- **MCPWM_FH1_CLR_OST:** A rising edge will clear on going one-shot mode action. (R/W)
  
- **MCPWM_FH1_CBCPULSE:** Cycle-by-cycle mode action refresh moment selection.
  - When all bits are TEZ/TEP, bit0 is set to 1: TEZ
  - When all bits are TEP, when bit1 is set to 1:
    (R/W)
  
- **MCPWM_FH1 FORCE CBC:** A toggle triggers a cycle-by-cycle mode action. (R/W)
  
- **MCPWM_FH1 FORCE OST:** A toggle (software negate its value) triggers a one-shot mode action.
  - The description indicates that it is read-only.

**Section Header:**
Register 36.43. MCPWM_FH1_STATUS_REG (0x00A8)

**Binary Representation Table for Register 36.43:**
- Binary bits are displayed in a table format with labels such as "MCPWM_FH1_CBC_ON", etc.
- The binary representation is shown from bit positions to the least significant bit.

**Description of Register 36.43 (MCPWM_FH1_STATUS_REG):**

- **MCPWM_FH1 CBC ON:** Set and reset by hardware, indicating that a cycle-by-cycle mode action is ongoing when set.
  
- **MCPWM_FH1 OST ON:** Set and reset by hardware to indicate an on-going one-shot mode action.

**Footer:**
Espressif Systems
Page number 1391 (ESP32-S3 TRM, Version 1.7)
Link for Submit Documentation Feedback