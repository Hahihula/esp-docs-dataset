**Title:**
Chapter 11 System Timer (SYSTIMER)

**GoBack Link:** GoBack

---

**Register Information and Description**

- **Register Name**: SYSTIMER_UNITO_VALUE_HI_REG (0x0040)
  - **Description**: 
    - **Field**: (reserved) to bit position: [31, 20]
    - **SYSTIMER_TIMER UNITO VALUE_HI**
    - **Read Value Description**:
      - High 20 bits.
      - **Register Name**: SYSTIMER_TIMER_UNITO_VALUE_HI
      - **Access Mode**: Read (R)

- **Register Name**: SYSTIMER_UNITO_VALUE_LO_REG (0x0044)
  - **Description**:
    - Low 32 bits read value for UNITO.
    - **Register Name**: SYSTIMER_TIMER_UNITO_VALUE_LO
    - **Access Mode**: Read (R)

- **Register Name**: SYSTIMER_UNITO_LOAD_REG (0x005C)
  - **Description**:
    - UNITO synchronization enable signal. Set this bit to reload the values of SYSTIMER_UNITO_LOAD_HI and SYSTIMER_TIMER_UNITO_LOAD_LO into UNITO.
    - **Register Name**: SYSTIMER_TIMER_UNITO_LOAD
    - **Access Mode**: Write (W)

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)