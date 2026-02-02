**Chapter Title:**
Motor Control PWM (MCPWM)

**Section Header:**
Register 29.55, PWM_FH2_CFGO_REG (0x00d8)

**Table Description:**
- The table lists various registers related to PWM_FH2_CFGO_REG with their bit positions and descriptions.
- Bits are labeled from '31' down to '0'.
- Each register is described in terms of its function when a fault event occurs or the timer value changes.

**Register Descriptions (with detailed explanations):**

1. **PWM_FH2_Bca Ost_U**
   - One-shot mode action on PWM2B when a fault event occurs and the timer is increasing.
   - Values: 0: do nothing, 1: force low, 2: force high, 3: toggle.

2. **PWM_FH2_Bca Ost_D**
   - One-shot mode action on PWM2B when a fault event occurs and the timer value decreases to zero or below it.
   - Values: 0: do nothing, 1: force low, 2: force high, 3: toggle.

3. **PWM_FH2_Bca Cbc U**
   - Cycle-by-cycle mode action on PWM2B when a fault event occurs and the timer is increasing to zero or below it.
   - Values: 0: do nothing, 1: force low, 2: force high, 3: toggle.

4. **PWM_FH2_Bca Cbc D**
   - Cycle-by-cycle mode action on PWM2B when a fault event occurs and the timer value decreases to zero or below it.
   - Values: 0: do nothing, 1: force low, 2: force high, 3: toggle.

5. **PWM_FH2_Aca Ost U**
   - One-shot mode action on PWM2A when a fault event occurs and the timer is increasing to zero or below it.
   - Values: 0: do nothing, 1: force low, 2: force high, 3: toggle.

6. **PWM_FH2_Aca Ost D**
   - One-shot mode action on PWM2A when a fault event occurs and the timer value decreases to zero or below it.
   - Values: 0: do nothing, 1: force low, 2: force high, 3: toggle.

7. **PWM_FH2_Aca Cbc U**
   - Cycle-by-cycle mode action on PWM2A when a fault event occurs and the timer is increasing to zero or below it.
   - Values: 0: do nothing, 1: force low, 2: force high, 3: toggle.

8. **PWM_FH2_Aca Cbc D**
   - Cycle-by-cycle mode action on PWM2A when a fault event occurs and the timer value decreases to zero or below it.
   - Values: 0: do nothing, 1: force low, 2: force high, 3: toggle.

9. **PWM_FH2_Fo Ost**
   - Event_f0 will trigger one-shot mode action on PWM2A when a fault event occurs and the timer is increasing to zero or below it.
   - Values: 0: disable, 1: enable (R/W).

10. **PWM_FH2_F1 Ost**
    - Event_f1 will trigger cycle-by-cycle mode action on PWM2A with an increase in the timer value from a low state back to high after reaching zero or below it.
    - Values: 0: disable, 1: enable (R/W).

11. **PWM_FH2_F2 Ost**
    - Event_f2 will trigger cycle-by-cycle mode action on PWM2A with an increase in the timer value from a low state back to high after reaching zero or below it.
    - Values: 0: disable, 1: enable (R/W).

12. **PWM_FH2_Sw Ost**
    - Enable register for software-forced one-shot mode action on PWM2A when an event occurs and the timer is increasing from a low state back to high after reaching zero or below it.
    - Values: 0: disable, 1: enable (R/W).

13. **PWM_FH2_Fo Cbc**
    - Event_f0 will trigger cycle-by-cycle mode action on PWM2A when an event occurs and the timer is increasing from a low state back to high after reaching zero or below it.
    - Values: 0: disable, 1: enable (R/W).

14. **PWM_FH2_F1 Cbc**
    - Event_f1 will trigger cycle-by-cycle mode action on PWM2A when an event occurs and the timer is increasing from a low state back to high after reaching zero or below it.
    - Values: 0: disable, 1: enable (R/W).

15. **PWM_FH2_F2 Cbc**
    - Event_f2 will trigger cycle-by-cycle mode action on PWM2A when an event occurs and the timer is increasing from a low state back to high after reaching zero or below it.
    - Values: 0: disable, 1: enable (R/W).

16. **PWM_FH2_Sw Cbc**
    - Enable register for software-forced cycle-by-cycle mode action on PWM2A when an event occurs and the timer is increasing from a low state back to high after reaching zero or below it.
    - Values: 0: disable, 1: enable (R/W).

**Footer Information:**
- Page number: 712
- Document version: ESP32 TRM (Version 5.6)
- Company name: Espressif Systems

**Link Description:** 
- Submit Documentation Feedback