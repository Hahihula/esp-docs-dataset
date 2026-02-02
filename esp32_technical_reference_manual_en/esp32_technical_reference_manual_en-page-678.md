**Chapter 29: Motor Control PWM (MCPWM)**

---

| Name | Description | P W M O | P W M1 | Acc |
|------|-------------|--------|--------|-----|
| **PWM_TIMER_SYNCI_CFG_REG** | Synchronization input selection for timers | 0x3FF5E034 | 0x3FF6C034 | R/W |
| **PWM_OPERATOR_TIMERSEL_REG** | Select specific timer for PWM operators | 0x3FF5E038 | 0x3FF6C038 | R/W |

---

### PWM Operator O Configuration and Status

- **PWM_GENO_STMP_CFG_REG**: Transfer status and update method for time stamp registers A and B
- **PWM_GENO_TSTMP_A_REG**: Shadow register for register A (Address: 0x3FF5E040, Access: R/W)
- **PWM_GENO_TSTMP_B_REG**: Shadow register for register B (Address: 0x3FF5E044, Access: R/W)
- **PWM_GENO_CFGO_REG**: Fault event TO and T1 handling
- **PWM_GENO_FORCEREG**: Permissives to force PWMQA and PWMQOB outputs by software

---

### Actions triggered by events on P W M O A

- **PWM_GENO_A_REG**: Actions (Address: 0x3FF5E050, Access: R/W)
- **PWM_GENO_B_REG**: Actions
- **PWM_DTO_CFG_REG**: Dead time type selection and configuration (Address: 0x3FF5E058, Access: R/W)

---

### Actions triggered by events on P W M O B

- **PWM_DTO_FED_CFG_REG** | Shadow register for falling edge delay (FED) (Address: 0x3FF5E05C, Access: R/W)
- **PWM_DTO_RED_CFG_REG**: Shadow register for rising edge delay (RED)

---

### Carrier enable and configuration

- **PWM_CARRIERO_CFG_REG**

---

### Actions on P W M O A and P W M O B on trip events

- **PWM_FHO_CFGO_REG** | Actions
- **PWM_FHO_CFG1_REG**: Software triggers for fault handler actions (Address: 0x3FF5E06C, Access: R/W)

---

### Status of fault events

- **PWM_FHO_STATUS_REG**

---

### PWM Operator 1 Configuration and Status

#### Transfer status and update method for time stamp registers A and B

- **PWM_GEN1_STMP_CFG_REG**: Actions (Address: 0x3FF5E074, Access: R/W)
- **PWM_GEN1_TSTMP_A_REG**: Shadow register for register A
- **PWM_GEN1_TSTMP_B_REG**: Shadow register for register B
- **PWM_GEN1_CFGO_REG**: Fault event TO and T1 handling

---

### Permissives to force P W M 1A and PWM1B outputs by software

- **PWM_GEN1_FORCEREG**

---

### Actions triggered by events on P W M 1A

- **PWM_GEN1_A_REG** | Actions
- **PWM_GEN1_B_REG**: Actions (Address: 0x3FF5E08C, Access: R/W)

---

### Dead time type selection and configuration

- **PWM_DT1_CFG_REG**

---

### Shadow register for FED

- **PWM_DT1_FED_CFG_REG** | Actions
- **PWM_DT1_RED_CFG_REG**: Shadow register for RED (Address: 0x3FF5E098, Access: R/W)

---

*Espressif Systems*

*ESP32 TRM (Version 5.6)*

*Submit Documentation Feedback*