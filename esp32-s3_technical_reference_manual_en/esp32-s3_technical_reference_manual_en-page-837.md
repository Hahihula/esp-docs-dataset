**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**Section Header:**
Register 1713. SYSTEM_RSA_PD_CTRL_REG (0x040)

**Binary Representation and Description of Register:**
- Binary representation shown with bits labeled from right to left.
- Explanation:
  - `SYSTEM_RSA_MEM_PD`: Set this bit to send the RSA memory into retention state, having lowest priority meaning it can be masked by the `SYSTEM_RSA_MEM_FORC PU` field. When Digital Signature occupies the RSA, this bit is invalid (R/W).
  
**Binary Representation and Description of Another Bit:**
- Binary representation shown with bits labeled from right to left.
- Explanation:
  - `SYSTEM_RSA_MEM_FORC PU`: Set this bit to force the RSA memory to work as normal when the chip enters light sleep. This bit has second highest priority, meaning it overrides the `SYSTEM_RSA_MEM_PD` field (R/W).

**Binary Representation and Description of Another Bit:**
- Binary representation shown with bits labeled from right to left.
- Explanation:
  - `SYSTEM_RSA_MEM_FORC PD`: Set this bit to send the RSA memory into retention state. This bit has highest priority, meaning it sends the RSA memory into retention state regardless of the `SYSTEM_RSA_MEM_FORC PU` field (R/W).

**Section Header:**
Register 1714. SYSTEM_EDMA_CTRL_REG (0x0044)

**Binary Representation and Description of Register:**
- Binary representation shown with bits labeled from right to left.
- Explanation:
  - `SYSTEM_EDMA_CLK_ON`: Set this bit to enable EDMA clock, having read/write access.

**Binary Representation and Description of Another Bit:**
- Binary representation shown with bits labeled from right to left.
- Explanation:
  - `SYSTEM_EDMA_RESET`: Set this bit to reset EDMA. Having read/write access (R/W).

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version:**
ESP32-S3 TRM (Version 1.7)