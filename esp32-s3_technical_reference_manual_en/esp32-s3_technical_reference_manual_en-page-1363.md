**Chapter 36: Motor Control PWM (MCPWM)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| MCPWM_GEN2_TSTMP_B_REG | PWM generator 2 shadow register for timer stamp B | 0x00B4 | R/W |
| MCPWM_GEN2_CFGO_REG | PWM generator 2 event T0 and T1 handling | 0x00B8 | R/W |
| MCPWM_GEN2 FORCE REG | Permissive to force PWM2A and PWM2B outputs by software | 0x00BC | R/W |
| MCPWM_GEN2 A REG | Actions triggered by events on PWM2A | 0x00C0 | R/W |
| MCPWM_GEN2 B REG | Actions triggered by events on PWM2B | 0x00C4 | R/W |
| MCPWM_DT2_CFG_REG | PWM generator 2 dead time type selection and configuration | 0x00C8 | R/W |
| MCPWM_DT2 FED_CFG_REG | PWM generator 2 shadow register for falling edge delay (FED) | 0x00CC | R/W |
| MCPWM_DT2 RED_CFG_REG | PWM generator 2 shadow register for rising edge delay (RED) | 0x00D0 | R/W |
| MCPWM_CARRIER2_CFG_REG | PWM generator 2 carrier enable and configuration | 0x00D4 | R/W |
| MCPWM_FH2_CFGO_REG | Actions on PWM2A and PWM2B trip events | 0x00D8 | R/W |
| MCPWM_FH2_CFG1_REG | Software triggers for fault handler actions | 0x00DC | R/W |
| MCPWM_FH2_STATUS_REG | Status of fault events | 0x00E0 | RO |
| Fault Detection Configuration and Status | Fault detection configuration and status | 0x00E4 | varies |

---

**Capture Configuration and Status**

- MCPWM_CAP_TIMER_CFG_REG: Configure capture timer
- MCPWM_CAP_TIMER_PHASE_REG: Phase for capture timer sync (R/W)
- MCPWM_CAP_CHO_CFG_REG: Capture channel 0 configuration and enable (varies R/W)
- MCPWM_CAP_CH1_CFG_REG: Capture channel 1 configuration and enable (varies RO)
- MCPWM_CAP_CH2_CFG_REG: Capture channel 2 configuration and enable (varies RO)
- MCPWM_CAP_CHO_REG: Ch0 capture value status register
- MCPWM_CAP_CH1_REG: Ch1 capture value status register
- MCPWM_CAP_CH2_REG: ch2 capture value status register

**Enable update of active registers**

- MCPWM_UPDATE_CFG_REG: Enable update (R/W)

---

**Manage Interrupts**

- MCPWM_INT_ENA_REG: Interrupt enable bits | 0x0110 | R/W
- MCPWM_INT_RAW_REG: Raw interrupt status /SS | 0x0114 | RW/TC

**Masked interrupt status**

- MCPWM_INT_ST_REG: Masked interrupt status (RO)

**Interrupt clear bits**

- MCPWM_INT_CLR_REG: Interrupt clear bits (WT)

---

**MCPWM APB Configuration Register**

- MCPWM_CLK_REG: MCPWM APB configuration register | 0x0120 | R/W

---

**Version Register**

- MCPWM_VERSION_REG: Version control register | 0x0124 | R/W

---

*Espressif Systems*
*ESP32-S3 TRM (Version 1.7)*
*Submit Documentation Feedback*

Page number at the bottom of page:
1363