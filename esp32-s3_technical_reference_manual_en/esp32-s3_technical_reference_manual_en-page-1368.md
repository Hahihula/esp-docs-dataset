**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

---

**Section Header:**
Register 36.8. MCPWM_TIMER1_SYNC_REG (0x01C)

**Diagram Description:**
- A binary diagram showing the layout of register bits with labels such as `MCPWM_TIMER1_SYNCO`, `MCPWM_TIMER1_SYNC`, and others.

**Field Descriptions for Register 36.8:**

- **MCPWM_TIMER1_SYNCI_EN (R/W)**
  - When set, timer reloading with phase on sync input event is enabled.
  
- **MCPWM_TIMER1_SYNC_SVG (R/W)**
  - Toggling this bit will trigger a software sync.

- **MCPWM_TIMER1_SYNCO_SEL (R/W)**
  - PWM timer1 sync_out selection. 
    - `0`: sync_in
    - `1`: TEZ
    - `2`: TEP
  - The `sync_out` will always generate when toggling the reg_timer1_sync_sw bit.

- **MCPWM_TIMER1_PHASE (R/W)**
  - Phase for timer reload on sync event.
  
- **MCPWM_TIMER1_PHASE_DIRECTION (R/W)**
  - Configure the PWM timer1's direction when timer1 is in up-down mode. 
    - `0`: increase
    - `1`: decrease

---

**Section Header:**
Register 36.9. MCPWM_TIMER1_STATUS_REG (0x020)

**Diagram Description:**
- A binary diagram showing the layout of register bits with labels such as `MCPWM_TIMER1_VALUE`, and others.

**Field Descriptions for Register 36.9:**

- **MCPWM_TIMER1_VALUE (RO)**
  - Current value of PWM timer1 counter.
  
- **MCPWM_TIMER1_DIRECTION (RO)**
  - Current direction of PWM timer1 countermovement:
    - `0`: increment
    - `1`: decrement

---

**Footer:**
Espressif Systems, Submit Documentation Feedback ESP32-S3 TRM (Version 1.7), Page number "1368"