**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**GoBack Link:** GoBack

---

**Section Header:**
Register 31.3. TWAI BUS_TIMING_1_REG (0x001C)

**Table Description for Register 31.3, TWAI BUS_TIMING_1_REG**

- **Field Name**: TWAL_TIME_SAMP
  - **Description**: The width of PBS2.
  - **Access Mode**: (RO | R/W)
  
- **Field Name**: TWAI_TIME_SEG1
  - **Description**: The width of PBS1.
  - **Access Mode**: (RO | R/W)

- **Field Name**: TWAI_TIME_SAMP
  - **Description**: The number of sample points. 
    - Option: O, the bus is sampled once; I, the bus is sampled three times (RO | R/W)
  
**Register Header for Register 31.4**
Register 31.4. TWAI_ERR_WARNING_LIMIT_REG (0x0034)

---

**Section Header:**
TWAI_ERR_WARNING_LIMIT_T

**Table Description for Register 31.4, TWAI_ERR_WARNING_LIMIT_REG**

- **Field Name**: TWAI_ERR_WARNING_LIMIT_T
  - **Description**: Error warning threshold.
    - In the case when any of an error counter value exceeds the threshold, or all the error counter values are below the threshold,
      an error warning interrupt will be triggered (given the enable signal is valid). 
    - Access Mode: (RO | R/W)

---

**Footer Information**
- **Company**: Espressif Systems
- **Page Number**: 1215
- **Document Version**: ESP32-S3 TRM (Version 1.7)
- **Link**: Submit Documentation Feedback