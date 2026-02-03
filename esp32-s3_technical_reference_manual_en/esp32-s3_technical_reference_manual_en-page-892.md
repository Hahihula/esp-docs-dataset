**Title:**
Chapter 21 HMAC Accelerator (HMAC)

**Section Title:**
21.5 Registers

**Body Text:**
The addresses in this section are relative to HMAC Accelerator base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Subsection with Register Information:**

- **Register Name:** Register 21.1. HMAC_SET_START_REG (0x040)
  - Description: Set this bit to start hmac operation.
  - Access Type: WO
  - Bit Positions Diagram:
    ```
    [31] [reserved] ... [0]
    ```

- **Register Name:** Register 21.2. HMAC_SET_PARA PURPOSE REG (0x044)
  - Description: Set HMAC parameter purpose, please see Table 21.2-1.
  - Access Type: WO
  - Bit Positions Diagram:
    ```
    [31] ... [4]
    ```

- **Register Name:** Register 21.3. HMAC_SET_PARA KEY REG (0x048)
  - Description: Set HMAC parameter key. There are six keys with index 0 ~ 5. Write the index of the selected key to this field.
  - Access Type: WO
  - Bit Positions Diagram:
    ```
    [31] ... [3]
    ```

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)