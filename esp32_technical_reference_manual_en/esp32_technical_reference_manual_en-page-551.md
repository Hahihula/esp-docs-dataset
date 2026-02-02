**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**GoBack Link:** GoBack

---

**Section Header: Register 25.2. TWAI BUS TIMING O_REG (0x0018)**

- **Field Name and Description:**
  - `TWAI_BAUD_PRESC`: Baud Rate Prescaler, determines the frequency dividing ratio.
    - Access Mode: Read/Write
  - `TWAI_SYNC_JUMP_WIDTH`: Synchronization Jump Width (SJW), ranging from 1 to 4 times wide.
    - Access Mode: Read/Write

**Binary Representation Diagram:** 
- A binary representation of a register with bits labeled and corresponding values.

---

**Section Header: Register 25.3. TWAI BUS TIMING I_REG (0x001C)**

- **Field Name and Description:**
  - `TWAI_TIME_SEG1`: The width of PBS1.
    - Access Mode: Read/Write
  - `TWAI_TIME_SEG2`: The width of PBS2.
    - Access Mode: Read/Write
  - `TWAI_TIME_SAMP`: The number of sample points. Options include:
    - 0: the bus is sampled once; 
    - 1: the bus is sampled three times.

**Binary Representation Diagram:** 
- A binary representation of a register with bits labeled and corresponding values, including fields for `TWAI_TIME_SEG1`, `TWAI_TIME_SEG2`, and `TWAI_TIME_SAMP`.

---

**Section Header: Register 25.4. TWAI ERR WARNING LIMIT REG (0x0034)**

- **Field Name and Description:**
  - `TWAI_ERR_WARNING_LIMIT`: Error warning threshold.
    - In the case when any of a error counter value exceeds the threshold, or all the error counter values are below the threshold,
      an error warning interrupt will be triggered (given the enable signal is valid).
    - Access Mode: Read/Write

**Binary Representation Diagram:** 
- A binary representation of a register with bits labeled and corresponding values.

---

**Footer Information:**
Espressif Systems
Page Number 551
ESP32 TRM (Version 5.6)
Submit Documentation Feedback