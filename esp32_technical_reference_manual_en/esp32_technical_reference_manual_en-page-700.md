**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Title:**
Register 29.36. PWM_GEN1_B_REG (0x00c8)

**Diagram Description:**
A binary register diagram with labels for each bit position from 31 to 0, and corresponding descriptions:
- `PWM_GEN1_B_DT1`
- `PWM_GEN1_B_DT0`
- `PWM_GEN1_B_DTEB`
- `PWM_GEN1_B_DTEA`
- `PWM_GEN1_B_DTEP`
- `PWM_GEN1_B_DTEZ`
- `PWM_GEN1_B_UT1`
- `PWM_GEN1_BUTO`
- `PWM_GEN1IBUTEP`
- `PWM_GEN1IBUTEA`
- `PWM_GEN1IBUTEB`
- `PWM_GEN1IBUTED`

**Text Descriptions:**
- **PWM_GEN1_B_DT1**: Action on PWM1B triggered by event_t1 when the timer decreases. 0: no change, 1: low, 2: high, 3: toggle. (R/W)
- **PWM_GEN1_B_DT0**: Action on PWM1B triggered by event_t0 when the timer decreases. (R/W)
- **PWM_GEN1_B_DTEB**: Action on PWM1B triggered by event TEB when the timer decreases. (R/W)
- **PWM_GEN1_B_DTEA**: Action on PWM1B triggered by event TEA when the timer decreases. (R/W)
- **PWM_GEN1_B_DTEP**: Action on PWM1B triggered by event TEP when the timer decreases. (R/W)
- **PWM_GEN1_B_DTEZ**: Action on PWM1B triggered by event TEZ when the timer decreases. (R/W)
- **PWM_GEN1_B_UT1**: Action on PWM1B triggered by event_t1 when the timer increases. (R/W)
- **PWM_GEN1IBUT0**: Action on PWM1B triggered by event_t0 when the timer increases. (R/W)
- **PWM_GEN1IBUTEP**: Action on PWM1B triggered by event TEP when the timer increases. (R/W)
- **PWM_GEN1IBUTEA**: Action on PWM1B triggered by event TEA when the timer increases. (R/W)

**Footer:**
Espressif Systems
700 ESP32 TRM (Version 5.6) Submit Documentation Feedback