**Title:**
Chapter 19 AES Accelerator (AES)

**Subtitle:**
19.8 Registers

**Body Text:**
The addresses in this section are relative to the AES accelerator base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Table Entries with Descriptions:**

1. **Register 19.1. AES_KEY_n_REG (η: 0-7) (0x0000+4*η)**
   - Address Range: 0x00000000
   - Description: Stores AES keys.
   - Access Mode: Read/Write

2. **Register 19.2. AES_TEXT_IN_m_REG (m: 0-3) (0x0020+4*m)**
   - Address Range: 0x00000000
   - Description: Stores the source data when the AES Accelerator operates in the Typical AES working mode.
   - Access Mode: Read/Write

3. **Register 19.3. AES_TEXT_OUT_m_REG (m: 0-3) (0x0030+4*m)**
   - Address Range: 0x00000000
   - Description: Stores the result data when the AES Accelerator operates in the Typical AES working mode.
   - Access Mode: Read Only

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback  
Page Number: ESP32-S3 TRM (Version 1.7)