**Chapter Title:**
Chapter 11 System Timer (SYSTIMER)

**GoBack Link:** GoBack

---

**Register Information and Description:**

- **Register Name**: SYSTIMER_UNIT1_VALUE_HI_REG (0x0048)
  - **Description**: 
    - **Binary Representation Diagram**: Shows a binary representation with bits labeled from 31 to 0.
    - **Text**: "SYSTIMER_TIMER UNIT1 VALUE HI" is written above the diagram, indicating that this register holds high value for the timer unit.

- **Register Name**: SYSTIMER_UNIT1_VALUE_LO_REG (0x004C)
  - **Description**:
    - **Binary Representation Diagram**: Similar to the previous one but labeled as "SYSTIMER_TIMER UNIT1 VALUE LO".
    - **Text**: "SYSTIMER_TIMER UNIT1 VALUE LO" is written above this diagram, indicating that this register holds low value for the timer unit.

- **Register Name**: SYSTIMER_UNIT1_VALUE_LO (0x0060)
  - **Description**:
    - This section describes how to read values from these registers.
    - The text mentions "SYSTIMER_TIMER UNIT1 VALUE LO" and indicates that it is a read value, low 32 bits.

- **Register Name**: SYSTIMER_UNIT1_LOAD_REG (0x0060)
  - **Description**:
    - This register allows for synchronization enable signal.
    - The text explains to set this bit to reload the values of SYSTIMER_TIMER UNIT1 LOAD_HI and SYSTIMER_TIMER UNIT1 LOAD_LO into UNIT1.

---

**Footer Information:**
- Page number: "645"
- Document version information: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems
- Link for submitting documentation feedback: Submit Documentation Feedback