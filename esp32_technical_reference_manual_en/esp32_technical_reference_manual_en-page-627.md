**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Register Information:**
- **Register Name:** IDINTEN_REG (0x0090)
- **Register Address:** Not explicitly provided, but referenced in the text.

**Field Descriptions and Values for IDINTEN_REG:**

1. **IDINTEN[AI] Abnormal Interrupt Summary Enable. (R/W)**
   - When set, an abnormal interrupt is enabled.
   - This bit enables:
     - IDINTEN[2]: Fatal Bus Error Interrupt;
     - IDINTEN[4]: DU Interrupt.

2. **IDINTEN[NI] Normal Interrupt Summary Enable. (R/W)**
   - When set, a normal interrupt is enabled.
   - When reset, a normal interrupt is disabled.
   - This bit enables:
     - IDINTEN[0]: Transmit Interrupt;
     - IDINTEN[1]: Receive Interrupt.

3. **IDINTEN[CES] Card Error Summary Interrupt Enable. (R/W)**
   - When set, it enables the Card Interrupt summary.

4. **IDINTEN[DU] Descriptor Unavailable Interrupt. (R/W)**
   - When set along with Abnormal Interrupt Summary Enable, the DU interrupt is enabled.
   - This bit also affects:
     - IDINTEN[FBE]: Fatal Bus Error Enable
       - When reset, Fatal Bus Error Enable Interrupt is disabled.

5. **IDINTEN[RI] Receive Interrupt Enable. (R/W)**
   - When set with Normal Interrupt Summary Enable, Receive Interrupt is enabled.
   - When reset, Receive Interrupt is disabled.

6. **IDINTEN[TI] Transmit Interrupt Enable. (R/W)**
   - When set with Normal Interrupt Summary Enable, Transmit Interrupt is enabled.
   - When reset, Transmit Interrupt is disabled.

**Additional Register Information:**

- **Register Name:** DSCADDR_REG (0x0094)
  - This register points to the start address of the current descriptor read by the IDMAC. It updates during operation and clears on reset:
    - **Field Description:** Host Descriptor Address Pointer

**Footer Information:**
- Page number: 627
- Document version: ESP32 TRM (Version 5.6)
- Company name: Espressif Systems
- Link to submit documentation feedback.

**Diagram/Block Diagrams:**

There is a diagram showing the bit layout of IDINTEN_REG with labels for each field and their corresponding values, but no specific details are provided in text form other than what has been described above.