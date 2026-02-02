**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.39. EMACADDR6HIGH_REG (0x1070)

**Diagram Description and Table:**

- **ADDRESS_ENABLE6:** 
  - When this bit is set, the address filter module uses the seventh MAC address for perfect filtering.
  - When this bit is reset, the address filter module ignores the address for filtering. (R/W)
  
- **SOURCE_ADDRESS6:** 
  - When this bit is set, the EMACADDR6[47:0] is used to compare with the SA fields of the received frame.

**MASK BYTE CONTROL6 Description and Table:**
- These bits are mask control bits for comparison of each of the EMACADDR6 bytes.
- When set high, the MAC does not compare the corresponding byte of received DA or SA with the contents of EMACADDR6 registers. Each bit controls the masking of the bytes as follows:
  - **Bit[29]:** EMACADDR6 High [15:8].
  - **Bit[28]:** EMACADDR6 High [7:0].
  - **Bit[27]:** EMACADDR6 Low [31:24].
  - **Bit[24]:** EMACADDR6 Low [7:0].

- You can filter a group of addresses (known as group address filtering) by masking one or more bytes of the address. (R/W)

**MAC_ADDRESS6_HI Description and Table:**
- This field contains the upper 16 bits, Bits[47:32] of the seventh 6-byte MAC address.
- Address fields are used for perfect matching.

**Section Header:**
Register 24.40. EMACADDR6LOW_REG (0x1074)

**Diagram Description and Table:**

- **EMACADDR6LOW_REG:** 
  - This field contains the lower 32 bits of the seventh 6-byte MAC address.
  - The content of this field is undefined, so the register needs to be configured after the initialization process. (R/W) 

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version:** ESP32 TRM (Version 5.6)
**Page Number:** 520