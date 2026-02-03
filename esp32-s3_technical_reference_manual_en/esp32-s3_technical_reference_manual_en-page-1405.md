**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Header:**
Register 36.68. MCPWM_UPDATE_CFG_REG (0x10C)

**Binary Diagram Description:**
A binary diagram is shown with the label "reserved" at position [31]. The rest of the positions are labeled as follows:
- MCPWM_OP2FORCE_UP_EN
- MCPWM_OP1FORCE_UP_EN
- MCPWM_OP0FORCE_UP_EN

**Body Text and Descriptions for Each Register:**

- **MCPWM_GLOBAL_UP_EN**
  - Description: The global enable of update of all active registers in MCPWM module.
  - Access Type (R/W)

- **MCPWM_GLOBAL FORCE_UP**
  - Description: A toggle (software invert its value) will trigger a forced update of all active registers in MCPWM module. 
  - Access Type (R/W)

- **MCPWM_OPO_UP_EN**
  - Description: When set and PWM_GLOBAL_UP_EN is set, update of active registers in PWM operator 0 are enabled.
  - Access Type (R/W)

- **MCPWM_OFOFORCE_UP**
  - Description: A toggle (software invert its value) will trigger a forced update of active registers in PWM operator O. 
  - Access Type (R/W)

- **MCPWM_OP1UP_EN**
  - Description: When set and PWM_GLOBAL_UP_EN is set, update of active registers in PWM operator 1 are enabled.
  - Access Type (R/W)

- **MCPWM_OP1FORCE_UP**
  - Description: A toggle (software invert its value) will trigger a forced update of active registers in PWM operator 1. 
  - Access Type (R/W)

- **MCPWM_OP2UP_EN**
  - Description: When set and PWM_GLOBAL_UP_EN is set, update of active registers in PWM operator 2 are enabled.
  - Access Type (R/W)

- **MCPWM_OP2FORCE_UP**
  - Description: A toggle (software invert its value) will trigger a forced update of active registers in PWM operator 2. 
  - Access Type (R/W)

**Footer Information:**
Espressif Systems
Page number and document version:
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback