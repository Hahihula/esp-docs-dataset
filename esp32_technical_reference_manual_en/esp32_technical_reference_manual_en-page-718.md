**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
Register 29.68. PWM_UPDATE_CFG_REG (0x10c)

**Binary Diagram Description:**
A binary diagram is provided showing the layout of bits in a register, with labels such as "PWM_OP2_FORCE_UP_EN", "PWM_OP1 FORCE_UP_EN", etc.

**Text Descriptions and Definitions for Each Bit Field:**

- **PWM_OP2FORCE_UP**: A toggle (software negation of this bit's value) will trigger a forced update of active registers in PWM operator 2. (R/W)
  
- **PWM_OP2UP_EN**: When set and PWM_GLOBAL_UP_EN is set, updates of active registers in PWM operator 2 are enabled. (R/W)

- **PWM_OP1FORCE_UP**: A toggle (software negation of this bit's value) will trigger a forced update of active registers in PWM operator 1. (R/W)
  
- **PWM_OP1UP_EN**: When set and PWM_GLOBAL_UP_EN is set, updates of active registers in PWM operator 1 are enabled. (R/W)

- **PWM_OPOFORCE_UP**: A toggle (software negation of this bit's value) will trigger a forced update of active registers in PWM operator O. (R/W)
  
- **PWM_OP0UP_EN**: When set and PWM_GLOBAL_UP_EN is set, updates of active registers in PWM operator 0 are enabled. (R/W)

- **PWM_GLOBALFORCE_UP**: A toggle (software negation of this bit's value) will trigger a forced update date of all active registers in the MCPWM module. (R/W)
  
- **PWM_GLOBALUP_EN**: The global enable of updates for all active registers in the MCPWM module.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version Information:**
718 ESP32 TRM (Version 5.6)