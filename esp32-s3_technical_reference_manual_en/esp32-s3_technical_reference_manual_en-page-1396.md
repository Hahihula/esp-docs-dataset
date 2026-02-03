**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Menu/Navigation Link:**
GoBack

**Table Title:**
Register 36.51. MCPWM_GEN2_B_REG (0x0044)

**Table Content Description:**
The table lists various registers related to the MCPWM_GEN2_B, each with a specific bit range and description.

**Body Text/Descriptions of Registers:**

- **MCPWM_GEN2_B_UTED**
  - Action on PWM2B triggered by event TEZ when timer increasing. 
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

- **MCPWM_GEN2_B_UTEP**
  - Action on PWM2B triggered by event TEP when timer increasing.
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

- **MCPWM_GEN2_B_UTFA**
  - Action on PWM2B triggered by event TEA when timer increasing. 
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

- **MCPWM_GEN2_B_UTEB**
  - Action on PWM2B triggered by event TEB when timer increasing. 
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

- **MCPWM_GEN2_BUTO**
  - Action on PWM2B triggered by event_t0 when timer increasing. 
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

- **MCPWM_GEN2_BTUTI**
  - Action on PWM2B triggered by event_t1 when timer increasing. 
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

- **MCPWM_GEN2_BDTED**
  - Action on PWM2B triggered by event TEZ when timer decreasing. 
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

- **MCPWM_GEN2_BTDEP**
  - Action on PWM2B triggered by event TEP when timer decreasing. 
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

- **MCPWM_GEN2_BDTEA**
  - Action on PWM2B triggered by event TEA when timer decreasing. 
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

- **MCPWM_GEN2_BTDEB**
  - Action on PWM2B triggered by event TEB when timer decreasing. 
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

- **MCPWM_GEN2_BDTTO**
  - Action on PWM2B triggered by event_t0 when timer decreasing. 
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

- **MCPWM_GEN2_BTDTI**
  - Action on PWM2B triggered by event_t1 when timer decreasing. 
  - 0: no change
  - 1: low; 2: high, 3: toggle.
  - (R/W)

**Footer Information:**
Espressif Systems  
Page number and document version:
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback