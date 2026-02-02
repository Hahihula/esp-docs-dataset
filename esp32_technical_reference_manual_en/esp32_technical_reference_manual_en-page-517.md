**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.33. EMACADDR3HIGH_REG (0x1058)

**Table Description:**
- **Columns:** ADDRESS_ENABLE3, SOURCE_ADDRESS3, MASK_BYTE_CONTROL3, MAC_ADDRESS3_HI
- **Rows:** 
  - Address: 31 30 29 24 23 16 15 (reserved) 0 Reset
  - Values for each bit position are listed.

**Text Content and Descriptions:**

1. **ADDRESS_ENABLE3**
   - When this bit is set, the address filter module uses the fourth MAC address for perfect filtering.
   - When this bit is reset, the address filter module ignores the address for filtering (R/W).

2. **SOURCE_ADDRESS3**
   - When this bit is set, the EMACADDR3[47:0] is used to compare with the SA fields of the received frame.
   - When this bit is reset, the EMACADDR3[47:0] is used to compare with the DA fields of the received frame. (R/W)

3. **MASK_BYTE_CONTROL3**
   - These bits are mask control bits for comparison of each of the EMACADDR3 bytes.
   - When set high, the MAC does not compare the corresponding byte of received DA or SA with the contents of EMACADDR3 registers.

4. **Bit Descriptions:**
   - Bit[29]: EMACADDR3 High [15:8].
   - Bit[28]: EMACADDR3 High [7:0].
   - Bit[27]: EMACADDR3 Low [31:24].
   - Bit[24]: EMACADDR3 Low [7:0].

**Additional Information about MAC_ADDRESS3_HI**
- This field contains the upper 16 bits, Bits[47:32] of the fourth 6-byte MAC address. (R/W)

**Section Header:**
Register 24.34. EMACADDR3LOW_REG (0x105C)

**Text Content and Descriptions:**

- **EMACADDR3LOW_REG**
   - This field contains the lower 32 bits of the fourth 6-byte MAC address.
   - The content of this field is undefined, so the register needs to be configured after the initialization process. (R/W)

**Footer Information:**
Espressif Systems
517 ESP32 TRM (Version 5.6)
Submit Documentation Feedback