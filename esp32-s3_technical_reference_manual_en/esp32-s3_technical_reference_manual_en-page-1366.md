**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
Register 36.4. MCPWM_TIMERO_SYNC_REG (0x00C)

**Table Description for Register 36.4:**
- **Columns:** 
  - Bits [31, 21, 20, ..., 0]
- **Values in Table:**
  - The table shows binary values and their corresponding descriptions.
  
**Field Descriptions within the Table (for MCPWM_TIMERO_SYNCI_EN):**
- When set, timer reloading with phase on sync input event is enabled. 
- Access type: Read/Write

**Field Description for Register 36.4 continued:**
- **MCPWM_TIMERO_SYNC_SW:** Toggling this bit will trigger a software sync.
- **MCPWM_TIMERO_SYNCO_SEL:** PWM timer0 sync_out selection, with options:
  - `0`: sync_in
  - `1`: TEZ (Trigger Edge Zero)
  - `2`: TEP (Trigger Edge Pulse)
- The `sync_out` will always generate when toggling the MCPWM_TIMERO_SYNC_SW bit.
- **MCPWM_TIMERO_PHASE:** Phase for timer reload on sync event. Read/Write
- **MCPWM_TIMERO_PHASE_DIRECTION:** Configure the PWM timer0’s direction when timer0 mode is up-down mode:
  - `0`: increase
  - `1`: decrease

**Section Header:**
Register 36.5. MCPWM_TIMERO_STATUS_REG (0x0010)

**Table Description for Register 36.5:**
- **Columns:** 
  - Bits [31, 17, ..., 0]
- **Values in Table:**
  - The table shows binary values and their corresponding descriptions.

**Field Descriptions within the Table (for MCPWM_TIMERO_VALUE):**
- Current PWM timer0 counter value. Read Only

**Field Description for Register 36.5 continued:**
- **MCPWM_TIMERO_DIRECTION:** Current PWM timer0 counter direction.
  - `0`: increment
  - `1`: decrement.

**Footer Information:**
Espressif Systems  
Page number and document version:
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback