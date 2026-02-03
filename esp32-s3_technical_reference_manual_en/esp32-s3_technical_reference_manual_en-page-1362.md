**Chapter 36: Motor Control PWM (MCPWM)**

---

### Table of Contents:

- **PWM Operator 1 Configuration and Status**
- **PWM Operator 2 Configuration and Status**

---

#### Section Title:
**PWM Operator 1 Configuration and Status**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| MCPWM_GENO FORCE REG | Permissive to force PWM0A and PWM0B outputs by software | 0x004C | R/W |
| MCPWM_GENO A REG | Actions triggered by events on PWM0A | 0x0050 | R/W |
| MCPWM_GENO B REG | Actions triggered by events on PWM0B | 0x0054 | R/W |
| MCPWM_DTO_CFG REG | PWM generator O dead time type selection and configuration | 0x0058 | R/W |
| MCPWM_DTO_FED_CFG REG | PWM generator O shadow register for falling edge delay (FED) | 0x005C | R/W |
| MCPWM_DTO_RED_CFG REG | PWM generator O shadow register for rising edge delay (RED) | 0x0060 | R/W |
| MCPWM_CARRIERO_CFG REG | PWM generator O carrier enable and configuration | 0x0064 | R/W |
| MCPWM_FHO_CFGO REG | Actions on PWM0A and PWM0B on trip events | 0x0068 | R/W |
| MCPWM_FHO_CFG1 REG | Software triggers for fault handler functions | 0x006C | R/W |
| MCPWM_FHO_STATUS REG | Status of fault events | 0x0070 | RO |

---

#### Section Title:
**PWM Operator 2 Configuration and Status**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| MCPWM_GEN1_STMP_CFG REG | Transfer status and update method for time stamp registers A and B | 0x0074 | varies |
| MCPWM_GEN1_TSTMP_A REG | PWM generator 1 shadow register for timer stamp A | 0x0078 | R/W |
| MCPWM_GEN1_TSTMP_B REG | PWM generator 1 shadow register for timer stamp B | 0x007C | R/W |
| MCPWM_GEN1_CFGO REG | PWM generator 1 event TO and T1 handling | 0x0080 | R/W |
| MCPWM_GEN1_FORCE REG | Permissive to force PWM1A and PWM1B outputs by software | 0x0084 | R/W |
| MCPWM_GEN1_A REG | Actions triggered by events on PWM1A | 0x0088 | R/W |
| MCPWM_GEN1_B REG | Actions triggered by events on PWM1B | 0x008C | R/W |
| MCPWM_DT1_CFG REG | PWM generator 1 dead time type selection and configuration | 0x0090 | R/W |
| MCPWM_DT1_FED_CFG REG | PWM generator 1 shadow register for falling edge delay (FED) | 0x0094 | R/W |
| MCPWM_DT1_RED_CFG REG | PWM generator 1 shadow register for rising edge delay (RED) | 0x0098 | R/W |
| MCPWM_CARRIER1_CFG REG | PWM generator 1 carrier enable and configuration | 0x009C | R/W |
| MCPWM_FH1_CFGO REG | Actions on PWM1A and PWM1B trip events | 0x00AO | R/W |
| MCPWM_FH1_CFG1 REG | Software triggers for fault handler functions | 0x00A4 | R/W |
| MCPWM_FH1_STATUS REG | Status of fault events | 0x00A8 | RO |

---

#### Section Title:
**PWM Operator 2 Configuration and Status**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| MCPWM_GEN2_STMP_CFG REG | Transfer status and update method for time stamp registers A and B | 0x00AC | varies |
| MCPWM_GEN2_TSTMP_A REG | PWM generator 2 shadow register for timer stamp A | 0x00BO | R/W |

---

**Footer:**
Espressif Systems  
1362 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback