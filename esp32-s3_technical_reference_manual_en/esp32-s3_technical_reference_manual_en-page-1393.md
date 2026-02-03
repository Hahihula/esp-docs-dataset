**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**GoBack Link:** GoBack

---

**Section Header:**
Register 36.46. MCPWM_GEN2_STMP_A_REG (0x00B0)

**Description of Register:**
- **Name:** MCPWM_GEN2_A
- **Type:** PWM generator 2 time stamp A’s shadow register.
- **Access Mode:** Read/Write

**Register Bits Description:**
- **Bits Range:** [31, 16]
- **Reset Value:** All bits are set to '0'.
- **Bit Labeling:** (reserved)

---

**Section Header:**
Register 36.47. MCPWM_GEN2_STMP_B_REG (0x00B4)

**Description of Register:**
- **Name:** MCPWM_GEN2_B
- **Type:** PWM generator 2 time stamp B’s shadow register.
- **Access Mode:** Read/Write

**Register Bits Description:**
- **Bits Range:** [31, 16]
- **Reset Value:** All bits are set to '0'.
- **Bit Labeling:** (reserved)

---

**Section Header:**
Register 36.48. MCPWM_GEN2_CFGO_REG (0x0DB8)

**Description of Register:**
- **Name:** MCPWM_GEN2_T1_SEL
- **Type:** Source selection for PWM generator 2 event_t1, take effect immediately.
- **Access Mode:** Read/Write

**Register Bits Description:**
- **Bits Range:** [31, 0]
- **Reset Value:** All bits are set to '0'.
- **Bit Labeling:**
  - Bit 9
  - Bit 7 (MCPWM_GEN2_T1_SEL)
  - Bit 6 (MCPWM_GEN2_TO_SEL)
  - Bit 4 and below

**Description of Bits:**
- **MCPWM_GEN2_CFG_UPMETH**: Update method for PWM generator 2’s active register of configuration.
  - Value '0': immediately; when bit0 is set to 1: TEZ;
  - When bit1 is set to 1: sync; when bit3 is set to 1: disable the update.

- **MCPWM_GEN2_TO_SEL**: Source selection for PWM generator 2 event_t0, take effect.
  - Value '0': fault_event0
  - Value '1': fault_event1

---

**Footer Information:** 
Espressif Systems  
Page Number: 1393  
Document Title: ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback Link