**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

---

**Section Header:**
Register 36.25. MCPWM_DTO_RED_CFG_REG (0x060)

**Diagram Description and Labels for Register 36.25:**
- The diagram shows a bit map with labels indicating the bits from most significant to least significant.
- Bits are labeled as follows:
  - 1
  - 14, 13, 12, 11 (reserved)
  - 8, 7, 5, 4

**Register Description:**
MCPWM_DTO_RED
- Shadow register for RED. (R/W)

---

**Section Header:**
Register 36.26. MCPWM_CARRIERO_CFG_REG (0x0064)

**Diagram Description and Labels for Register 36.26:**
- The diagram shows a bit map with labels indicating the bits from most significant to least significant.
- Bits are labeled as follows:
  - 1
  - 8, 7, 5, 4 (reserved)
  - 0

**Register Description and Fields for Register 36.26:**
- MCPWM_CARRIERO_EN When set, carrier0 function is enabled. When cleared, carrier0 is by-passed.
- MCPWM_CARRIERO_PRESCALE PWM carrier0 clock (PC_clk) prescale value. Period of PC_clk = period of PWM_clk * (PWM_CARRIERO_PRESCALE + 1). (R/W)
- MCPWM_CARRIERO_DUTY Carrier duty selection. Duty = PWM_CARRIERO_DUTY/8.
- MCPWM_CARRIERO_OSHTWTH Width of the first pulse in number of periods of the carrier. (R/W)
- MCPWM_CARRIERO_OUT_INVERT When set, invert the output of PWMOA and PVMOB for this sub-module.

**Additional Fields:**
- MCPWM_CARRIERO_IN_INVERT
  - Description: Invert the input of PWMOA and PVMOB for this sub-module.
  - Access Type (R/W)

---

**Footer Information:** 
Espressif Systems  
Page Number: 1380  
Document Version: ESP32-S3 TRM (Version 1.7)  

**Links at Footer:**
- Submit Documentation Feedback