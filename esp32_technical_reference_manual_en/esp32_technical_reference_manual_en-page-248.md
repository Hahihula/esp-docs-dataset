**Title: Chapter 12 DPort Registers**

---

### Register Description

- **Register Name:** DPOR APPCPU_CTRL_REG_C_REG (0x34)
  
  - **Field:** `DPOR_APPCPU_RUNSTALL`
    - **Description:** Set to 1 to put APP_CPU into stalled state. Clear the bit to release APP_CPU from stalled state.
    - **Access Mode:** Read/Write
    - **Bit Positions and Values:**
      ```
      31 0
      ```

- **Register Name:** DPOR APPCPU_CTRL_REG_D_REG (0x38)
  
  - **Field:** `DPOR_APPCPU_RUNSTALL`
    - **Description:** When APP_CPU is booted up with ROM code, it will jump to the address stored in this register.
    - **Access Mode:** Read/Write
    - **Bit Positions and Values:**
      ```
      31 0
      ```

- **Register Name:** DPOR_CPU_PER_CONF_REG (0x3C)
  
  - **Field:** `DPOR_CPU_CPU_PERIOD_SEL`
    - **Description:** Select CPU clock. Refer to Table 7.2-2 for details.
    - **Access Mode:** Read/Write
    - **Bit Positions and Values:**
      ```
      31 0
      ```

---

**Footer Information**

- Page Number: `248`
- Document Title: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems

[Submit Documentation Feedback](#)