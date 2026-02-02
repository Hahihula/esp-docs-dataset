**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
Register 29.7. PWM_TIMER1_CFG1_REG (0x0018)

**Field Description and Values for PWM_TIMER1_CFG1_REG:**

- **PWM_TIMER1_MOD**: 
  - Value Range: [0, 3]
  - Description:
    - `0`: freeze
    - `1`: increase mode
    - `2`: decrease mode (R/W)
  
- **PWM_TIMER1_START**:
  - Value Range: [1]
  - Description:
    - `1`: if PWM timer1 starts, then stops at TEP; 
    - `2`: PWM timer1 starts and runs on;
    - `3`: PWM timer1 starts and stops at the next TEZ.
  
- **PWM_TIMER1_START** (Repeated):
  - Value Range: [4]
  - Description:
    - `4`: PWM timer1 starts and stops at the next TEP. (R/W)

**Section Header:**
Register 29.8. PWM_TIMER1_SYNC_REG (0x001c)

**Field Description and Values for PWM_TIMER1_SYNC_REG:**

- **PWM_TIMER1_PHASE_DIR**:
  - Value Range: [0, 1]
  - Description:
    - `0`: increase
    - `1`: decrease.
  
- **PWM_TIMER1_PHASE** (Repeated):
  - Value Range: [R/W]
  - Description:
    - Phase for timer reload at sync event.

- **PWM_TIMER1_SYNCO_SEL**:
  - Value Range: [0, TEZ; TEP; otherwise:]
  - Description:
    - `sync_out` is always O. (R/W)
  
- **PWM_TIMER1_SYNC_SW**:
  - Description:
    - Toggling this bit will trigger a software sync.
  
- **PWM_TIMER1_SYNCI_EN**:
  - Value Range: [R/W]
  - Description:
    - When set, timer reloading with phase at sync input event is enabled.

**Footer Information:**
Espressif Systems
Page Number: 683
Document Version: ESP32 TRM (Version 5.6)
Link Texts: Submit Documentation Feedback