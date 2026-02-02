**Title: Chapter 9 Low-Power Management (RTC_CNTL)**

**GoBack**

---

**Subtitle: Register 9.7. RTC_CNTL_STATEO_REG (0x0018)**

- **Field Description:** 
  - `31` to `24`: Reserved bits.
  - `23`: RTC_CNTL_SLP_REJECT
    - Sleep reject bit, R/W access mode.

**Bit Positions and Labels:**
- `31` (MSB): Reset
- `0` (LSB): Reset

**Field Descriptions for Specific Bits in the Register:**

- **RTC_CNTL_SLEEP_EN**: Sleep enable bit. Access is Read/Write.
- **RTC_CNTL_SLP_REJECT**: Sleep reject bit, access mode R/W.

---

**Subtitle: Register 9.8. RTC_CNTL_TIMER1_REG (0x001C)**

- **Field Description:** 
  - `31`: Reserved bits for the register.

**Bit Positions and Labels:**
- `31` (MSB): Reset
- `0` (LSB): Reset
  
**Field Descriptions for Specific Bits in the Register:**

- **RTC_CNTL_CPUSTALL_EN**: CPU stall enable bit, access mode Read/Write. 

---

**Footer Information:**  
Espressif Systems  
ESP32 TRM (Version 5.6)  

**Link:** Submit Documentation Feedback