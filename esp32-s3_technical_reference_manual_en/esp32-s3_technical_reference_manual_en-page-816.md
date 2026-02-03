**Chapter Title:**
Chapter 16 World Controller (WCL)

**GoBack Link:** GoBack

**Register Information for WCL_CORE_0_MESSAGE_PHASE_REG (0x0108):**

- **Field Description and Values:**
  - `31` to `0`: Reserved bits.
  
- **Field Details with Descriptions in Markdown format:**
  - **WCL_CORE_0_MESSAGE_MATCH:** Indicates if CPUO’s world switch is successful. This field is only used for debugging (RO).
  - **WCL_CORE_0_MESSAGEEXPECT:** Indicates the number to be written next for CPUO. This field is only used for debugging (RO).
  - **WCL_CORE_0_MESSAGE_DATAPHASE:** When `1`, indicates CPUO is checking if the agreed sequence is written to clear write_buffer. This field is only used for debugging (RO).
  - **WCL_CORE_0_MESSAGE_ADDRESSPHASE:** When `1`, indicates CPUO is checking if any sequence is written to the agreed address to clear write_buffer. This field is only used for debugging (RO).

**Register Information for WCL_CORE_0_STATUSUTABLEn_REG (n: 1-13) (0x0080+4*(n-1)):**

- **Field Description and Values:**
  - `31` to `0`: Reserved bits.
  
- **Field Details with Descriptions in Markdown format:**
  - **WCL_CORE_0_FROM_WORLD:** Stores the world info for CPUO before entering entry `n`. (R/W)
  - **WCL_CORE_0_FROM ENTRY:** Stores the previous entry info for CPUO before entering entry `n`. (R/W)
  - **WCL_CORE_0_CURRENT Entry n:** Indicates if the interrupt is at entry `n` for CPUO. (R/W)

**Footer:**
- Page number and document version information:
  - "816 ESP32-S3 TRM (Version 1.7)"
  
- Company name:
  - Espressif Systems
  
- Links:
  - Submit Documentation Feedback