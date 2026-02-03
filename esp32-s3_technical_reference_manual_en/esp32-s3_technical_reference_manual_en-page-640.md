**Chapter Title:**
Chapter 11 System Timer (SYSTIMER)

**GoBack Link:** GoBack

---

### Table of Contents:

- **Name**: SYSTIMER UNIT0 VALUE LO REG, SYSTIMER UNIT0 LOAD REG  
  - Description:
    - SYSTIMER UNIT0 VALUE LO REG
      - Address: 0x044 RO
      - Access: UNIT0 value, low 32 bits
    - SYSTIMER UNIT0 LOAD REG
      - Address: 0x05C WT
      - Access: UNIT0 synchronization register

- **UNIT1 Control and Configuration Registers**:
  - SYSTIMER UNIT1_OP_REG (Read UNIT1 value to registers)
    - Address: varies
    - Access: R/W
  - SYSTIMER UNIT1 LOAD HI REG, SYSTIMER UNIT1 LOAD LO REG 
    - Description for each register is similar with addresses and access modes.
  - SYSTIMER UNIT1 VALUE HI REG (UNIT1 value, high 20 bits)
    - Address: varies RO

- **Comparator Control and Configuration Registers**:
  - SYSTIMER TARGET0 HI REG
    - Alarm value to be loaded to COMP0, high 20 bits R/W 
    - Address: 0x0C1
  - SYSTIMER TARGET0 LO REG (Alarm value to be loaded to COMP0, low 32 bits)
    - Address: varies RO

- **SYSTIMER TARGET0 CONF REG**
  - Configure COMPO alarm mode WT
  - Address: varies R/W

- **SYSTIMER COMPO LOAD REG**:
  - COMPO synchronization register 
  - Address: varies WT

- **Comparator Control and Configuration Registers (SYSTIMER TARGET1)**:
  - SYSTIMER TARGET1 HI REG, SYSTIMER TARGET1 LO REG
    - Alarm value to be loaded to COMP1, high 20 bits R/W
    - Address ranges are provided for each register.

- **SYSTIMER TARGET1 CONF REG**
  - Configure COMP1 alarm mode WT
  - Address: varies RO

- **SYSTIMER COMP1 LOAD REG**:
  - COMP1 synchronization register 
  - Address range is given as WT

- **Comparator Control and Configuration Registers (SYSTIMER TARGET2)**:

- **Interrupt Registers**:
  - SYSTIMER INT ENA REG, SYSTIMER INT RAW REG
    - Interrupt enable register of system timer R/W
    - Address: varies RO
  - SYSTIMER INT CLR REG 
    - Interrupt clear register of system timer WT
    - Address range is provided.

- **SYSTIMER INT ST REG**:
  - Interrupt status register of system timer RO

- **COMP0 Status Registers**:  
  - SYSTIMER REAL TARGET0 LO REG, SYSTIMER REAL TARGET0 HI REG 
    - Actual target value of COMP0 R/W
    - Address ranges are provided.

- **COMP1 Status Registers**:

- **SYSTIMER REAL TARGET1 LO REG, SYSTIMER REAL TARGET1 HI REG**
  - Actual target value of COMP1 RO

- **COMP2 Status Registers**:  
  - SYSTIMER REAL TARGET2 LO REG (Actual target value of COMP2 R/W)
    - Address ranges are provided.

### Version Register:
- SYSTIMER_DATE_REG
  - Version control register 
  - Access: varies RW

---

**Footer Information:**  
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

**Link for Feedback Submission**: Submit Documentation Feedback