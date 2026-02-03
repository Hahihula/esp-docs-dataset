**Title:**
Chapter 36 Motor Control PWM (MCPWM)

**Back Link:**
GoBack

**Register Information:**
- Register Name: MCPWM_GEN2 FORCE REG (0x0BC)
- Bit Positions and Values:
  - 15, 14 to 9 are set as "reserved"
  - Other bits from bit8 down have specific functions related to different modes of operation.

**Bit Definitions Table:**

| Bit | Description |
|-----|-------------|
| 31 | (reserved) |
| ... | ... |
| 0  | Reset |

**Descriptions for Each Bit Field in the Register:**

- **MCPWM_GEN2_CNTUFORCE_UPMETHOD**
  - Updating method for continuous software force of PWM generator 2. When all bits are set to O: immediately; when bit0 is set to 1: TEZ; when bit1 is set to 1: TEP; when bit2 is set to 1: TEA; when bit3 is set to 1: TEB; when bit4 is set to 1: sync; when bit5 is set to 1: disable update. (TEA/B here and below means an event generated when the timer's value equals to that of register A/B.) 

- **MCPWM_GEN2_A_CNTUFORCE_MODE**
  - Continuous software force mode for PWM2A.
  - Values:
    - Low, high; disabled.

- **MCPWM_GEN2_B_CNTUFORCE_MODE**
  - Continuous software force mode for PWM2B. 
  - Values: Same as above

- **MCPWM_GEN2_A_NCIFORCE_MODE**
  - Trigger of non-continuous immediate software-force event for PWM2A.
  - A toggle will trigger a force event.

- **MCPWM_GEN2_A_NCIFORCE_MODE**
  - Non-continuous immediate software force mode for PWM2A. 
  - Values: Same as above

- **MCPWM_GEN2_B_NCIFORCE_MODE**
  - Trigger of non-continuous immediate software-force event for PWM2B.
  - A toggle will trigger a force event.

- **MCPWM_GEN2_B_NCIFORCE_MODE**
  - Non-continuous immediate software force mode for PWM2B. 
  - Values: Same as above

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type:
  - ESP32-S3 TRM (Version 1.7)
- Page Number: 1394
- Link to Submit Documentation Feedback