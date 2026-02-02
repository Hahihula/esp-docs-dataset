**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.35. EMACADDR4HIGH_REG (0x1060)

**Diagram Description and Table of Bits in EMACADDR4HIGH_REG:**
- The diagram shows a bit map for the register with labels such as ADDRESS_ENABLE4, SOURCE_ADDRESS4, MASK_BYTE_CONTROL4.
- Bit positions are labeled from 31 to 0.

**Text Content under Diagrams:**

- **ADDRESS_ENABLE4:** When this bit is set, the address filter module uses the fifth MAC address for perfect filtering. When this bit is reset, the address filter ignores the address for filtering (R/W).

- **SOURCE_ADDRESS4:** When this bit is set, the EMACADDR4[47:0] is used to compare with the SA fields of the received frame. When this bit is reset, the EMACADDR4[47:0] is used to compare with the DA fields of the received frame (R/W).

- **MASK_BYTE_CONTROL4:** These bits are mask control bits for comparison of each of the EMACADDR4 bytes. When set high, the MAC does not compare the corresponding byte of received DA or SA with the contents of EMACADDR4 registers. Each bit controls the masking of the bytes as follows:
  - Bit[29]: EMACADDR4 High [15:8].
  - Bit[28]: EMACADDR4 High [7:0].
  - Bit[27]: EMACADDR4 Low [31:24].
  - Bit[24]: EMACADDR4 Low [7:0].

**Additional Information about MAC_ADDRESS4_HI and MAC_ADDRESS4_LO:**
- **MAC_ADDRESS4_HI:** This field contains the upper 16 bits, Bits[47:32] of the fifth 6-byte MAC address (R/W).
- **MAC_ADDRESS4_LO:** The lower part is not described in this visible section.

**Section Header for Another Register:**
Register 24.36. EMACADDR4LOW_REG (0x1064)

**Text Content under Section Header:**

- This field contains the lower 32 bits of the fifth 6-byte MAC address.
- The content of this field is undefined, so the register needs to be configured after the initialization process.

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Page Number:**
ESP32 TRM (Version 5.6)
Page number not visible in provided text