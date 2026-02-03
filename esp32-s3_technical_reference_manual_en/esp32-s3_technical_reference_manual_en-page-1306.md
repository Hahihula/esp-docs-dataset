**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**Back to Top Button:** GoBack

---

**Register Section Header:**
Register 34.34. SDHOST_IDINTEN_REG (0x0090)

**Binary Representation Diagram of Register:**

- The diagram shows a binary representation with bits labeled from `1` at the top, down through various positions to `0`.

**Field Descriptions in the Register:**
- **SDHOST_IDINTEN_AI:** Abnormal Interrupt Summary Enable. When set, an abnormal interrupt is enabled.
  - This bit enables:
    - IDINTEN[2]: Fatal Bus Error Interrupt; (R/W)
    - IDINTEN[4]: DU Interrupt.

- **SDHOST_IDINTEN_NI:** Normal Interrupt Summary Enable. 
  - When set, a normal interrupt is enabled.
  - When reset, a normal interrupt is disabled.
  - This bit enables the following bits:
    - IDINTEN[0]: Transmit Interrupt;
    - IDINTEN[1]: Receive Interrupt.

- **SDHOST_IDINTEN_CES:** Card Error summary Interrupt Enable. 
  - When set, it enables the Card Interrupt summary (R/W).

- **SDHOST_IDINTEN_DU:** Descriptor Unavailable Interrupt.
  - Summary Enable; when set along with Abnormal Interrupt Summary Enable, the DU interrupt is enabled.

- **SDHOST_IDINTEN_FBE:** Fatal Bus Error Interrupt Enable. 
  - When set with Abnormal Interrupt Summary Enable,
    - The Fatal Bus Error Interrupt is enabled (R/W).
  - When reset, Fatal Bus Error Enable Interrupt is disabled.
  
- **SDHOST_IDINTEN_RI:** Receive Interrupt Enable.
  - When set with Normal Interrupt Summary Enable;
    - Receive Interrupt is enabled. 
    - When reset, Receive Interrupt is disabled.

- **SDHOST_IDINTEN_TI:** Transmit Interrupt Enable.
  - Transmitted Interrupt is enabled when set; normal interrupt summary enable,
    - Transmitted Interrupt (R/W).

**Register Section Header:**
Register 34.35. SDHOST_DSCADDR_REG (0x0094)

**Binary Representation Diagram of Register:**

- The diagram shows a binary representation with bits labeled from `1` at the top, down through various positions to `0`.

**Field Description in the Register:**
- **SDHOST_DSCADDR_REG:** Host Descriptor Address Pointer.
  - Updated by IDMAC during operation and cleared on reset. 
  - This register points to the start address of the current descriptor read by the IDMAC (RO).

---

**Footer Information:**
Espressif Systems
1306 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback