**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
Register 36.61. MCPWM_CAP_CH0_CFG_REG (0xOFO)

**Table Description for Register 36.61:**
- **Columns:** Bits numbered from 32 to 0, with some bits labeled as "reserved."
- **Rows:** Each row corresponds to a bit in the register.
- **Bit Labels and Values:**
  - MCPWM_CAPO_EN (bit at position [31]: Reserved)
  - MCPWM_CAPO_MODE
    - Description for each value:
      - When set, capture on channel O after prescaling. When bit0 is set to 1: enable capture on the falling edge.
      - When bit1 is set to 1: enable capture on the rising edge (R/W)
  - MCPWM_CAPO_PRESCALE
    - Value of prescaling on rising edge of CAPO. Prescale value = PWM_CAPO_PRESCAL + 1.

**Section Header:**
Register 36.62. MCPWM_CAP_CH1_CFG_REG (0xOFO4)

**Table Description for Register 36.62:**
- **Columns:** Bits numbered from 32 to 0, with some bits labeled as "reserved."
- **Rows:** Each row corresponds to a bit in the register.
- **Bit Labels and Values:**
  - MCPWM_CAP1_EN (bit at position [31]: Reserved)
  - MCPWM_CAP1_MODE
    - Description for each value:
      - When set, capture on channel 1 after prescaling. When bit0 is set to 1: enable capture on the falling edge.
      - When bit1 is set to 1: enable capture on the rising edge (R/W)
  - MCPWM_CAP1_PRESCALE
    - Value of prescaling on rising edge of CAP1. Prescale value = PWM_CAP1_PRESCAL + 1.

**Footer Information:**
Espressif Systems, ESP32-S3 TRM (Version 1.7), Submit Documentation Feedback

(Note: The text is transcribed as it appears in the image with respect to structure and content.)