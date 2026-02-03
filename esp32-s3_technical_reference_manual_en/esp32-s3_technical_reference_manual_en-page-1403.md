**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
Register 36.63. MCPWM_CAP_CH2_CFG_REG (0x00F8)

**Table Description for Register 36.63:**
- **Columns:** Binary representation of the register bits.
- **Bits Description:**
  - `MCPWM_CAP2_EN`: When set, capture on channel 2 is enabled. (R/W)
  - `MCPWM_CAP2_MODE`: Edge of capture on channel 2 after prescaling. When bit0 is set to 1: enable capture on the falling edge; when bit1 is set to 1: enable capture on the rising edge. (R/W)
  - `MCPWM_CAP2_PRESCALE`: Value of prescaling on rising edge of CAP2. Prescale value = PWM_CAP2_PRESCAL + 1. (R/W)
  - `MCPWM_CAP2_IN_INVERT`: When set, CAP2 form GPIO matrix is inverted before prescale. (R/W)
  - `MCPWM_CAP2_SW`: Write 1 will trigger a software forced capture on channel 2. (WT)

**Section Header:**
Register 36.64. MCPWM_CAP_CHO_REG (0x00FC)

**Table Description for Register 36.64:**
- **Columns:** Binary representation of the register bits.
- `MCPWM_CAPO_VALUE`: Value of last capture on channel O. (RO)
- `MCPWM_CAP_CH1_REG (0x0100)`

**Section Header:**
Register 36.65.

**Table Description for Register 36.65:**
- **Columns:** Binary representation of the register bits.
- `MCPWM_CAP1_VALUE`: Value of last capture on channel 1. (RO)

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Type:**
ESP32-S3 TRM (Version 1.7)