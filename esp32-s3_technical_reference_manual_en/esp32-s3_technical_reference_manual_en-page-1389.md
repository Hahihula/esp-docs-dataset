**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

---

**Section Header:**
Register 36.39. MCPWM_DT1_RED_CFG_REG (0x0098)

**Subsection Description:**
MCPWM_DT1_RED Shadow register for RED. (R/W)

**Binary Representation Table:**
- The table shows the binary representation of a value with bits labeled from most significant bit to least.
  - Bits are numbered starting at '31' on the left and decreasing towards '0'.
  - Each row represents different segments or fields within this register.

---

**Section Header:**
Register 36.40. MCPWM_CARRIER1_CFG_REG (0x009C)

**Subsection Description:**
MCPWM_CARRIER1_INVERT, MCPWM_CARRIER1_OUT_INVERT, MCPWM_CARRIER1_INVERT, MCPWM_CARRIER1_INVERT

**Binary Representation Table for Fields within Register 36.40:**
- The table shows the binary representation of a value with bits labeled from most significant bit to least.
  - Bits are numbered starting at '31' on the left and decreasing towards '0'.
  - Each row represents different segments or fields within this register.

**Field Descriptions for Register 36.40:**
- **MCPWM_CARRIER1_EN (R/W):** When set, carrier1 function is enabled. When cleared, carrier1 is bypassed.
- **MCPWM_CARRIER1_PRESCALE:** PWM carrier1 clock (PC_clk) prescale value. Period of PC_clk = period of PWM_clk * (PWM_CARRIER0_PRE SCALE + 1). (R/W)
- **MCPWM_CARRIER1_DUTY:** Carrier duty selection. Duty = PWM_CARRIER0_DUTY/8. (R/W)
- **MCPWM_CARRIER1_OSHTWTH:** Width of the first pulse in number of periods of the carrier. (R/W)
- **MCPWM_CARRIER1_OUT_INVERT:** When set, invert the output of PWM1A and PWM1B for this sub-module. (R/W)
- **MCPWM_CARRIER1_IN_INVERT:** When set, invert the input of PWM1A and PWM1B for this sub-module. (R/W)

---

**Footer:**
Espressif Systems
Page number 1389 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback