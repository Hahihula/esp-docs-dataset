**Chapter Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Section Header:**
GoBack

**Register Information for MCPWM_GENO_TSTMP_B_REG (0x0044):**

- **Description:** 
  - Register Number: 36.18.
  - Name: MCPWM_GENO_TSTMP_B_REG
  - Address: 0x0044

**Register Details for MCPWM_GENO_CFG0_REG (0x048):**
- **Description**: 
  - Register Number: 36.19.

**Field Descriptions in the Table under MCPWM_GENO_CFG_UPMETHD:**

| Field | Description |
|-------|-------------|
| `bit0` | TEZ; when bit0 is set to 1: TEZ |
| `bit1` | TEP; when bit2 is set to 1:sync; when bit3 is set to 1:disable the update |

**Field Descriptions in the Table under MCPWM_GENO_TO_SEL:**

- **Description**: 
  - Source selection for PWM generator O event_t0, take effect immediately.
  
| Field | Description |
|-------|-------------|
| `bit0` | fault_event0 |
| `bit1` | fault_event1 |
| `bit2` | fault_event2 |
| `bit3` | sync_taken |

**Field Descriptions in the Table under MCPWM_GENO_T1_SEL:**

- **Description**: 
  - Source selection for PWM generator O event_t1, take effect immediately.
  
| Field | Description |
|-------|-------------|
| `bit0` | fault_event0 |
| `bit1` | fault_event1 |
| `bit2` | fault_event2 |
| `bit3` | sync_taken |
| `bit4` | none |

**Footer:**
- Page Number: 1375
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems

**Link:** Submit Documentation Feedback