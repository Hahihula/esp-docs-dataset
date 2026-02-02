**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.41. EMACADDR7_HIGH_REG (0x1078)

**Diagram Description and Table:**
- Diagram shows the layout of register bits.
- Bits are labeled as follows:
  - ADDRESS_ENABLE7
  - SOURCE_ADDRESS7
  - MASK_BYTE_CONTROL7

**Text Content with Descriptions for Each Bit Field in EMACADDR7_HIGH_REG (0x1078):**

- **ADDRESS_ENABLE7**
  - When this bit is set, the address filter module uses the eighth MAC address for perfect filtering. 
  - When this bit is reset, the address filter module ignores the address for filtering.
  - Access: Read/Write

- **SOURCE_ADDRESS7**
  - When this bit is set, the EMACADDR7[47:0] is used to compare with the SA fields of the received frame. 
  - When this bit is reset, the EMACADDR7[47:0] is used to compare with the DA fields of the received frame.
  - Access: Read/Write

- **MASK_BYTE_CONTROL7**
  - These bits are mask control bits for comparison of each of the EMACADDR7 bytes. 
  - When set high, the MAC does not compare the corresponding byte of received DA or SA with the contents of EMACADDR7 registers.
  - Each bit controls the masking of the bytes as follows:
    - Bit[29]: EMACADDR7 High [15:8].
    - Bit[28]: EMACADDR7 High [7:0].
    - Bit[27]: EMACADDR7 Low [31:24].
    - Bit[24]: EMACADDR7 Low [7:0].

  You can filter a group of addresses (known as group address filtering) by masking one or more bytes of the address.
  - Access: Read/Write

- **MAC_ADDRESS7_HI**
  - This field contains the upper 16 bits, Bits[47:32] of the eighth 6-byte MAC address. 
  - Access: Read/Write

**Section Header:**
Register 24.42. EMACADDR7LOW_REG (0x107C)

**Text Content for EMACADDR7LOW_REG (0x107C):**

- This field contains the lower 32 bits of the eighth 6-byte MAC address.
- The content of this field is undefined, so the register needs to be configured after the initialization process. 
- Access: Read/Write

**Footer Information:**
Espressif Systems
Page Number: 521
Document Version: ESP32 TRM (Version 5.6)
Feedback Link Texts:
- Submit Documentation Feedback