**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.31. EMACADDR2HIGH_REG (0x1050)

**Field Description Table:**

- **ADDRESS_ENABLE2**: When this bit is set, the address filter module uses the third MAC address for perfect filtering. When this bit is reset, the address filter module ignores the address for filtering.
  - **Source:**
    - SOURCE_ADDRESS2
      - When this bit is set, the EMACADDR2[47:0] is used to compare with the SA fields of the received frame. When this bit is reset, the EMACADDR2[47:0] is used to compare with the DA fields of the received frame.
  - **MASK BYTE CONTROL2**: These bits are mask control bits for comparison of each of the EMACADDR2 bytes. When set high, the MAC does not compare the corresponding byte of received DA or SA with the contents of EMACADDR2 registers.

**Bit Description Table:**
- Bit[29]: EMACADDR2 High [15:8].
- Bit[28]: EMACADDR2 High [7:0].
- Bit[27]: EMACADDR2 Low [31:24].
- Bit[24]: EMACADDR2 Low [7:0].

**Additional Information:** 
You can filter a group of addresses (known as group address filtering) by masking one or more bytes of the address.

**Field Description Table for MAC_ADDRESS2_HI:**
This field contains the upper 16 bits, Bits[47:32] of the third 6-byte MAC address. The content is undefined after initialization process.
- **Source:** (R/W)

**Section Header:**
Register 24.32. EMACADDR2LOW_REG (0x1054)

**Field Description Table for EMACADDR2LOW_REG:**
This field contains the lower 32 bits of the third 6-byte MAC address.
- **Source:** The content is undefined, so the register needs to be configured after initialization process. 
- **Source:** (R/W) 

**Footer Information:**
Espressif Systems
516 ESP32 TRM (Version 5.6)
Submit Documentation Feedback