**Chapter Title:**
Chapter 24 Ethernet Media Process Controller (EMAC)

**GoBack Link:** GoBack

---

**Register Section Header:**

- **Register Name and Address:**
  - Register 24.29, EMACADDR1HIGH_REG (0x1048B)
  
- **Address Diagram Description:**
  - The diagram shows the address bits for register 24.29 with labels such as ADDRESS_ENABLE1, SOURCE_ADDRESS, MASK_BYTE_CONTROL, and MAC_ADDRESS1_HI.
  - Bits are numbered from right to left starting at bit 31.

**Register Details Table:**

- **ADDRESS_ENABLE1**
  - Description:
    - When this bit is set, the address filter module uses the second MAC address for perfect filtering. 
    - When this bit is reset, the address filter module ignores the address for filtering.
    - Access Mode (R/W): Read/Write

- **SOURCE_ADDRESS**
  - Description:
    - When this bit is set, the EMACADDR1[47:0] is used to compare with the SA fields of the received frame. 
    - When this bit is reset, the EMACADDR1[47:0] is used to compare with the DA fields of the received frame.
    - Access Mode (R/W): Read/Write

- **MASK_BYTE_CONTROL**
  - Description:
    - These bits are mask control bits for comparison of each of the EMACADDR1 bytes. 
    - When set high, the MAC does not compare the corresponding byte of received DA or SA with the contents of EMACADDR1 registers.
    - Each bit controls the masking of the bytes as follows:

      - **Bit[29]:** EMACADDR1 High [15:8].
      - **Bit[28]:** EMACADDR1 High [7:0].
      - **Bit[27]:** EMACADDR1 Low [31:24].
      - **Bit[24]:** EMACADDR1 Low [7:0].

    You can filter a group of addresses (known as group address filtering) by masking one or more bytes of the address.
    Access Mode (R/W): Read/Write

- **MAC_ADDRESS1_HI**
  - Description:
    - This field contains the upper 16 bits, Bits[47:32] of the second 6-byte MAC address. 
    - Access Mode (R/W): Read/Write

---

**Register Section Header Continued:**

- **Register Name and Address:**
  - Register 24.30, EMACADDR1LOW_REG (0x104C)

- **EMACADDR1LOW_REG Description:**
  - This field contains the lower 32 bits of the second 6-byte MAC address.
  - The content of this field is undefined; so the register needs to be configured after the initialization process. 
  - Access Mode (R/W): Read/Write

---

**Footer Information:**

- **Company:** Espressif Systems
- **Document Version and Link:** ESP32 TRM (Version 5.6)
- **Action Links:** Submit Documentation Feedback