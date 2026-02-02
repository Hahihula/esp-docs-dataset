**Chapter Title:**
Chapter 29 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

**Section Header and Description with Register Information:**

- **Register Name**: Register 29.60. PWM_CAP_TIMER_PHASE_REG (0x00ec)
  - **Description**: Phase value for the capture timer sync operation.
    - **Access Type**: Read/Write
    - **Value Example**: `o` Reset

- **Register Name**: Register 29.61. PWM_CAP_CHO_CFG_REG (0x00f0)
  - This section includes a table with various configuration bits and their descriptions:
    - **PWM_CAPO_SW**: When set, software-forced capture on channel O is triggered.
      - **Access Type**: Write Only
    - **PWM_CAPO_INVERT**: When set, CAPO form GPIO matrix is inverted before prescaling.
      - **Access Type**: Read/Write
    - **PWM_CAPO_PRESCALE**: Prescaling value on the positive edge of CAPO. Prescaling value = PWM_CAPO_PRESCALE + 1 (Read/Write)
    - **PWM_CAPO_MODE**: Edge capture on channel O after prescaling. When bit0 is set to 1: enable capture on the negative edge; when bit1 is set to 1: enable capture on the positive edge.
      - **Access Type**: Read/Write
    - **PWM_CAPO_EN**: When set, capture on channel O is enabled.

**Footer Information:** 
- Page number and document version:
  - "715 ESP32 TRM (Version 5.6)"
- Company name: Espressif Systems
- Link for submitting documentation feedback: Submit Documentation Feedback