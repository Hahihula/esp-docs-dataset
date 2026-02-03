**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Back to Top Link:** GoBack

---

**Section Header:**
Register 36.12. MCPWM_TIMER2_SYNC_REG (0x002C)

**Field Description Table for Register 36.12:**

| Bit | Name                          |
|-----|-------------------------------|
| 31-24| MCPWM_TIMER2_PHASE_DIRECTION  |
|     | (reserved)                    |

**Field Details and Descriptions:**  
MCPWM_TIMER2_SYNCI_EN
- When set, timer reloading with phase on sync input event is enabled.
- Access: Read/Write

MCPWM_TIMER2_SYNC_SW
- Toggling this bit will trigger a software sync. 
- Access: Read/Write

MCPWM_TIMER2_SYNCO_SEL
- PWM timer2 sync_out selection:
  - 0: sync_in;
  - 1: TEZ;
  - 2: TEP.
- The sync_out will always generate when toggling the reg_timer2_sync_sw bit. 
- Access: Read/Write

MCPWM_TIMER2_PHASE
- Phase for timer reload on sync event (up-down mode).
- Values:
  - 0: increase; 
  - 1: decrease;
- Access: Read/Write

---

**Section Header:**
Register 36.13. MCPWM_TIMER2_STATUS_REG (0x0030)

**Field Description Table for Register 36.13:**

| Bit | Name                          |
|-----|-------------------------------|
| 31-24| MCPWM_TIMER2_VALUE           |
|     | (reserved)                    |

**Field Details and Descriptions:**  
MCPWM_TIMER2_VALUE
- Current value of PWM timer2 counter.
- Access: Read Only

MCPWM_TIMER2_DIRECTION
- Current direction of PWM timer2 counter:
  - 0: increment;
  - 1: decrement. 
- Access: Read Only

---

**Footer Information:**  
Espressif Systems  
Page Number: 1371  
Document Version (Version 1.7)  

**Links for Additional Actions:**  
Submit Documentation Feedback