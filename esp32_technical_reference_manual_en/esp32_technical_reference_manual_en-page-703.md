**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**Section Header:**
Register 29.41. PWM_FH1_CFGO_REG (0x0a0xCU)

**Table Description:**
The table shows the register bits for PWM_FH1_CFGO_REG, with each bit labeled as follows:
- PWM_FH1_Aca Ost U
- PWM_FH1_Bca Ost D
- PWM_FH1_Cbc Ost C
- PWM_FH1_Aca Ost T
- PWM_FH1_Bca Ost O
- PWM_FH1_Cbc Ost R

**Text Descriptions:**
- **PWM_FH1_Bca Ost U:** One-shot mode action on PWM1B when a fault event occurs and the timer is increasing. 0: do nothing, 1: force low, 2: force high, 3: toggle (R/W)
- **PWM_FH1_Bca Ost D:** One-shot mode action on PWM1B when a fault event occurs and the timer is decreasing. 0: do nothing, 1: force low, 2: force high, 3: toggle (R/W)
- **PWM_FH1_Cbc Ost U:** Cycle-by-cycle mode action on PWM1B when a fault event occurs and the timer is increasing. 0: do nothing, 1: force low, 2: force high, 3: toggle (R/W)
- **PWM_FH1_Cbc Ost D:** Cycle-by-cycle mode action on PWM1B when a fault event occurs and the timer is decreasing. 0: do nothing, 1: force low, 2: force high, 3: toggle (R/W)
- **PWM_FH1_Aca Ost U:** One-shot mode action on PWM1A when a fault event occurs and the timer is increasing. 0: do nothing, 1: force low, 2: force high, 3: toggle (R/W)
- **PWM_FH1_Aca Ost D:** One-shot mode action on PWM1A when a fault event occurs and the timer is decreasing. 0: do nothing, 1: force low, 2: force high, 3: toggle (R/W)
- **PWM_FH1_Cbc Ost U:** Cycle-by-cycle mode action on PWM1A when a fault event occurs and the timer is increasing. 0: do nothing, 1: force low, 2: force high, 3: toggle (R/W)
- **PWM_FH1_Aca Ost D:** Cycle-by-cycle mode action on PWM1A when a fault event occurs and the timer is decreasing. 0: do nothing, 1: force low, 2: force high, 3: toggle (R/W)

**Additional Settings Descriptions:**
- **PWM_FH1_Fo Ost:** Enable event_f0 to trigger one-shot mode action.
- **PWM_FH1_F1 Ost:** Enable event_f1 to trigger one-shot mode action. 
- **PWM_FH1_F2 Ost:** Enable event_f2 to trigger cycle-by-cycle mode action.

**Enable Settings:**
- **PWM_FH1_Sw Ost:** Enable the register for software-forced one-shot mode action.
- **PWM_FH1_Fo CBC:** Enable event_f0 to trigger cycle-by-cycle mode action. 
- **PWM_FH1_F1 CBC:** Enable event_f1 to trigger cycle-by-cycle mode action.

**Additional Information:**
Espressif Systems
Submit Documentation Feedback

**Document Footer:**
ESP32 TRM (Version 5.6)