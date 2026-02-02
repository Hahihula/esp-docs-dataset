**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
Register 29.50. PWM_GEN2_B_REG (0x00c4C)

**Table Description:**
- The table shows the bits of a register with labels such as `PWM_GEN2_B_DT1`, `PWM_GEN2_B_DTO`, etc.
- Each bit is labeled from DTEA to UTEZ, and there are also reserved positions.

**Text Descriptions for Bits/Registers (in Markdown format):**

- **PWM_GEN2_B_DT1**: Action on PWM2B triggered by event_t1 when the timer decreases. 0: no change, 1: low, 2: high, 3: toggle. (R/W)
  
- **PWM_GEN2_B_DTO**: Action on PWM2B triggered by event_t0 when the timer decreases. (R/W)

- **PWM_GEN2_B_DTEN**: Action on PWM2B triggered by event TEB when the timer decreases. (R/W)

- **PWM_GEN2_B_DTENA**: Action on PWM2B triggered by event TEA when the timer increases. (R/W)

- **PWM_GEN2_B_DTENZ**: Action on PWM2B triggered by event TEZ when the timer decreases. (R/W)

- **PWM_GEN2_B_UT1**: Action on PWM2B triggered by event_t1 when the timer increases. (R/W)

- **PWM_GEN2_BUTO**: Action on PWM2B triggered by event_t0 when the timer increases. (R/W)

- **PWM_GEN2IBUTEN**: Action on PWM2B triggered by event TEB when the timer decreases. (R/W)

- **PWM_GEN2IBUTENA**: Action on PWM2B triggered by event TEA when the timer increases. (R/W)

- **PWM_GEN2IBUTENZ**: Action on PWM2B triggered by event TEZ when the timer increases. (R/W)

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback