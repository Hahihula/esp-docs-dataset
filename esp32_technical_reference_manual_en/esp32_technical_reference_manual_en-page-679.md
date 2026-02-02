**Chapter 29: Motor Control PWM (MCPWM)**

---

| Name | Description | PWO0 | PWM1 | Acc |
|------|-------------|------|------|-----|
| PWM_CARRIER1_CFG_REG | Carrier enable and configuration | 0x3FF5E0C9 | 0x3FF6C09C | R/W |
| PWM_FH1_CFG0_REG | Actions on PWM1A and PWM1B on fault events | 0x3FF5E0A0 | 0x3FF6C0A0 | R/W |
| PWM_FH1_CFG1_REG | Software triggers for fault handler actions | 0x3FF5E0A4 | 0x3FF6C0A4 | R/W |
| PWM_FH1_STATUS_REG | Status of fault events | 0x3FF5E0A8 | 0x3FF6C0A8 | RO |
| **PWM Operator 2 Configuration and Status** | | | | |
| PWM_GEN2_STMP_CFG_REG | Transfer status and updating method for time stamp registers A and B | 0x3FF5E0AC | 0x3FF6C0AC | R/W |
| PWM_GEN2_TSTMP_A_REG | Shadow register for register A | 0x3FF5E0B0 | 0x3FF6C0B0 | R/W |
| PWM_GEN2_TSTMP_B_REG | Shadow register for register B | 0x3FF5E0B4 | 0x3FF6C0B4 | R/W |
| PWM_GEN2_CFGO_REG | Fault event TO and T1 handling | 0x3FF5E080 | 0x3FF6C080 | R/W |
| PWM_GEN2 FORCE REG | Permissives to force PWM2A and PWM2B outputs by software | 0x3FF5E0BC | 0x3FF6COBC | R/W |
| PWM_GEN2_A_REG | Actions triggered by events on PWM2A | 0x3FF5E0C0 | 0x3FF6COCO | R/W |
| PWM_GEN2_B_REG | Actions triggered by events on PWM2B | 0x3FF5E0C4 | 0x3FF6COCA4 | R/W |
| PWM_DT2_CFG_REG | Dead time type selection and configuration | 0x3FF5E0C8 | 0x3FF6COCA8 | R/W |
| PWM_DT2_FED_CFG_REG | Shadow register for FED | 0x3FF5E0CC | 0x3FF6COCA4 | R/W |
| PWM_DT2_RED_CFG_REG | Shadow register for RED | 0x3FF5E0D0 | 0x3FF6C0DA0 | R/W |
| PWM_CARRIER2_CFG_REG | Carrier enable and configuration | 0x3FF5E0D4 | 0x3FF6COCA4 | R/W |
| PWM_FH2_CFGO_REG | Actions at PWM2A and PWM2B on trip events | 0x3FF5E0D8 | 0x3FF6C0DA8 | R/W |
| PWM_FH2_CFG1_REG | Software triggers for fault handler actions | 0x3FF5E0DC | 0x3FF6COCA4 | R/W |
| PWM_FH2_STATUS_REG | Status of fault events | 0x3FF5E0E0 | 0x3FF6C0EA0 | RO |
| **Fault Detection Configuration and Status** | | | | |
| PWM_FAULT_DETECT_REG | Fault detection configuration and status | 0x3FF5E0E4 | 0x3FF6COEA4 | R/W |
| **Capture Configuration and Status** | | | | |
| PWM_CAP_TIMER_CFG_REG | Configure capture timer | 0x3FF5E0E8 | 0x3FF6C0E8 | R/W |
| PWM_CAP_TIMER_PHASE_REG | Phase for capture timer sync | 0x3FF5E0EC | 0x3FF6COEC | RO |
| PWM_CAP_CHO_CFG_REG | Capture channel O configuration and enable | 0x3FF5E0F0 | 0x3FF6COFO | R/W |
| PWM_CAP_CH1_CFG_REG | Capture channel 1 configuration and enable | 0x3FF5E0F4 | 0x3FF6COFA4 | RO |
| PWM_CAP_CH2_CFG_REG | Capture channel 2 configuration and enable | 0x3FF5E0F8 | 0x3FF6COFA8 | R/W |
| PWM_CAP_CHO_REG | Value of last capture on channel O | 0x3FF5E0FC | 0x3FF6COFC | RO |
| PWM_CAP_CH1_REG | Value of last capture on channel 1 | 0x3FF5E100 | 0x3FF6C100 | R/W |
| PWM_CAP_CH2_REG | Value of last capture on channel 2 | 0x3FF5E104 | 0x3FF6C104 | RO |
| PWM_CAP_STATUS_REG | Edge of last capture trigger | 0x3FF5E108 | 0x3FF6C108 | R/W |

---

*Espressif Systems*

*ESP32 TRM (Version 5.6)*

*Submit Documentation Feedback*