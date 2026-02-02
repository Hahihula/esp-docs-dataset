**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
Register 29.62. PWM_CAP_CH1_CFG_REG (0x0f4)

**Binary Register Diagram for PWM_CAP_CH1_CFG_REG:**
- Bits are labeled from right to left as follows:
  - Reserved
  - PWM_CAP1_SW, Write 1 will trigger a software-forced capture on channel 1.
  - PWM_CAP1_INVERT When set, CAP1 form GPIO matrix is inverted before prescaling. (R/W)
  - PWM_CAP1_PRESCALE Value of prescale on the positive edge of CAP1. Prescale value = PWM_CAP1_PRESCALE + 1. (R/W)
  - PWM_CAP1_MODE Edge capture on channel 1 after prescaling. When bit0 is set to 1: enable capture on the negative edge; when bit1 is set to 1: enable capture on the positive edge.
  - PWM_CAP1_EN When set, capture on channel 1 is enabled.

**Section Header:**
Register 29.63. PWM_CAP_CH2_CFG_REG (0x0f8)

**Binary Register Diagram for PWM_CAP_CH2_CFG_REG:**
- Bits are labeled from right to left as follows:
  - Reserved
  - PWM_CAP2_SW When set, a software-forced capture on channel 2 is triggered.
  - PWM_CAP2_INVERT When set, CAP2 form GPIO matrix is inverted before prescaling. (R/W)
  - PWM_CAP2_PRESCALE Prescaling value on the positive edge of CAP2. Prescale value = PWM_CAP2_PRESCALE + 1. (R/W)
  - PWM_CAP2_MODE Edge capture on channel 2 after prescaling. When bit0 is set to 1: enable capture on the negative edge; when bit1 is set to 1: enable capture on the positive edge.
  - PWM_CAP2_EN When set, capture on channel 2 is enabled.

**Footer Information:**
Espressif Systems
716 ESP32 TRM (Version 5.6)
Submit Documentation Feedback