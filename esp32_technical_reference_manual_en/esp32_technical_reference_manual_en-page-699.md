**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Register Information:**
- Register Name: PWM_GEN1_A_REG (0x0088)
- Diagram Description:
  - The diagram shows a register layout with various fields labeled as follows from left to right and top to bottom, starting at the most significant bit on the far left.
    - PWM_GEN1_A_DT1
    - PWM_GEN1_A_DT0
    - PWM_GEN1_A_DTEA
    - PWM_GEN1_A_DTEB
    - PWM_GEN1_A_DTEP
    - PWM_GEN1_A_DTEZ
    - PWM_GEN1_A_UT1
    - PWM_GEN1_AUTO
    - PWM_GEN1 AUTEB
    - PWM_GEN1 AUTEA
    - PWM_GEN1 AUTEP
    - PWM_GEN1 AUTEZ

**Field Descriptions:**
- **PWM_GEN1_A_DT1**: Action on PWM1A triggered by event_t1 when the timer decreases. 0: no change, 1: low, 2: high, 3: toggle.
- **PWM_GEN1_A_DT0**: Action on PWM1A triggered by event_t0 when the timer decreases (R/W).
- **PWM_GEN1_A_DTEB**: Action on PWM1A triggered by event TEB when the timer decreases. (R/W)
- **PWM_GEN1 A DTEA**: Action on PWM1A triggered by event TEA when the timer decreases.
- **PWM_GEN1 A DTEP**: Action on PWM1A triggered by event TEP when the timer decreases
- **PWM_GEN1 A DTEZ**: Action on PWM1A triggered by event TEZ when the timer decreases (R/W)
- **PWM_GEN1_A_UT1**: Action on PWM1A triggered by event_t1 when the timer increases. (R/W).
- **PWM_GEN1 AUTO**: Action on PWM1A triggered by event_t0 when the timer increases.
- **PWM_GEN1 AUTEB**: Action on PWM1A triggered by event TEB when the timer increases
- **PWM_GEN1 AUTEA**: Action on PWM1A triggered by event TEA when the timer increases (R/W)
- **PWM_GEN1 AUTEP**: Action on PWM1A triggered by event TEP when the timer increases.
- **PWM_GEN1 AUTEZ**: Action on PWM1A triggered by event TEZ when the timer increases.

**Footer:**
- Espressif Systems
- Page Number: 699
- Document Version: ESP32 TRM (Version 5.6)
- Links:
  - Submit Documentation Feedback