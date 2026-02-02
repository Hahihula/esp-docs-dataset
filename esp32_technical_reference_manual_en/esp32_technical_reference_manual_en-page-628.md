**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

**Register Information Section**

- **Register Name and Address:**
  - Register 27.33. BUFADDR_REG (0x0098)
  
- **Description of BUFADDR_REG:**
  - "BUFADDR_REG Host Buffer Address Pointer, updated by IDMAC during operation and cleared on reset. This register points to the current Data Buffer Address being accessed by the IDMAC."
  - (RO)

---

**Register Information Section**

- **Register Name and Address:**
  - Register 27.34. CLK_EDGE_SEL (0x0800)
  
- **Description of CLK_EDGE_SEL:**
  - "This register is used to select the clock phase for different signals."

- **Table Description with Values:**
  - The table lists various registers related to clock edges and their descriptions:
    - `CCLKIN_EDGE_N`: This value should be equal to CCLKIN_EDGE_L. (R/W)
    - `CCLKIN_EDGE_L`: The low level of the divider clock. The value should be larger than CCLKIN_EDGE_H.
    - `CCLKIN_EDGE_H`: The high level of the divider clock. The value should be smaller than CCLKIN_EDGE_L.

- **Additional Registers:**
  - `CCLKIN_EDGE_SLF_SEL`: Used to select the clock phase of the internal signal from phase90, phase180, or phase270.
  - `CCLKIN_EDGE_SAM_SEL`: Used to select the clock phase of the input signal from phase90, phase180, or phase270.
  - `CCLKIN_EDGE_DRV_SEL`: Used to select the clock phase of the output signal from phase90, phase180, or phase270.

---

**Footer Information:**
- "Espressif Systems"
- Page number and document version:
  - "628 ESP32 TRM (Version 5.6)"
- Link for submitting documentation feedback.
  - "Submit Documentation Feedback"