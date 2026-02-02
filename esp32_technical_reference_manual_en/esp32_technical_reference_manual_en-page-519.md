**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.37. EMACADDR5HIGH_REG (0x1068)

**Table Description:**
- **Columns:** ADDRESS ENABLE, SOURCE_ADDRESS, MASK BYTE CONTROLS, MAC_ADDRESS5_HI
- **Rows:** 
  - Address ENABLE: 31 bits with values ranging from 0 to 2^31.
  - SOURCE_ADDRESS: 47 bits (0x0000000000000000 to 0xFFFFFFF).
  - MASK BYTE CONTROLS: 5 bytes, each bit controls the masking of specific parts as described below:
    - Bit[29]: EMACADDR5 High [15:8].
    - Bit[28]: EMACADDR5 High [7:0].
    - Bit[27]: EMACADDR5 Low [31:24].
    - Bit[24]: EMACADDR5 Low [7:0].

**Text Explanation for ADDRESS_ENABLE5:**
When this bit is set, the address filter module uses the sixth MAC address for perfect filtering. When this bit is reset, the address filter module ignores the address for filtering.

**Text Explanation for SOURCE_ADDRESS5:**
When this bit is set, the EMACADDR5[47:0] is used to compare with the SA fields of the received frame. When this bit is reset, the EMACADDR5[47:0] is used to compare with the DA fields of the received frame.

**Text Explanation for MASK_BYTE_CONTROL5:**
EMACADDR5 bytes. When set high, the MAC does not compare the corresponding byte of received DA or SA with the contents of EMACADDR5 registers. Each bit controls the masking of the bytes as follows:
- Bit[29]: EMACADDR5 High [15:8].
- Bit[28]: EMACADDR5 High [7:0].
- Bit[27]: EMACADDR5 Low [31:24].
- Bit[24]: EMACADDR5 Low [7:0].

You can filter a group of addresses (known as group address filtering) by masking one or more bytes of the address.

**Text Explanation for MAC_ADDRESS5_HI:**
This field contains the upper 16 bits, Bits[47:32] of the sixth 6-byte MAC address. It is read/write accessible.
  
**Section Header:**
Register 24.38. EMACADDR5LOW_REG (0x106C)

**Text Explanation for EMACADDR5LOW_REG:**
This field contains the lower 32 bits of the sixth 6-byte MAC address. The content of this field is undefined, so the register needs to be configured after the initialization process.

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version:** ESP32 TRM (Version 5.6)