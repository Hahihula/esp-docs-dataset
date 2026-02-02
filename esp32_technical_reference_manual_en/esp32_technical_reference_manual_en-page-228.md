**Chapter Title:**
Chapter 10 Timer Group (TIMG)

**GoBack Link:** GoBack

---

**Section Header: Register 10.4**

- **Register Name and Address:**
  - TIMGn_TUPDATE_REG (x: 0-1) (0xC+0x24*x)
  
- **Description of the Register:**
  - TIMGn_TUPDATE_REG
    - Write any value to trigger a timer x time-base counter value update (timer x current value will be stored in registers above). (WO)

---

**Section Header: Register 10.5**

- **Register Name and Address:**
  - TIMGn_TALARMLO_REG (x: 0-1) (0x10+0x24*x)
  
- **Description of the Register:**
  - TIMGn_TALARMLO_REG
    - Timer x alarm trigger time-base counter value, low 32 bits. (R/W)

---

**Section Header: Register 10.6**

- **Register Name and Address:**
  - TIMGn_TALARMHI_REG (x: 0-1) (0x14+0x24*x)
  
- **Description of the Register:**
  - TIMGn_TALARMHI_REG
    - Timer x alarm trigger time-base counter value, high 32 bits. (R/W)

---

**Section Header: Register 10.7**

- **Register Name and Address:**
  - TIMGn_TLOADLO_REG (x: 0-1) (0x18+0x24*x)
  
- **Description of the Register:**
  - TIMGn_TLOADLO_REG
    - Low 32 bits of the value that a reload will load onto timer x time-base counter. (R/W)

---

**Section Header: Register 10.8**

- **Register Name and Address:**
  - TIMGn_TLOADHI_REG (x: 0-1) (0x1C+0x24*x)
  
- **Description of the Register:**
  - TIMGn_TLOADHI_REG
    - High 32 bits of the value that a reload will load onto timer x time-base counter. (R/W)

---

**Footer Information:** 
Espressif Systems, Submit Documentation Feedback

**Document Version and Title:**
ESP32 TRM (Version 5.6)