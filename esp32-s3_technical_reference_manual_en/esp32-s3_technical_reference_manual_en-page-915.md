**Chapter Title:**
Chapter 23 External Memory Encryption and Decryption (XTS_AES)

**Section Header:**
23.6 Register Summary

**Body Text:**
The addresses in this section are relative to the External Memory Encryption and Decryption base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table Headers:**
- Name
- Description
- Address
- Access

**Table Content (Partial):**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| Plaintext Register Heap |  |         |        |
| XTS_AESPLAIN_0_REG | Plaintext register 0 | 0x0000 | R/W |
| XTS_AESPLAIN_1_REG | Plaintext register 1 | 0x0004 | R/W |
| ... | ... | ... | ... |

**Subsection Title:**
Configuration Registers

**List Items (Partial):**

- XTS_ALINESIZE_REG | Configures the size of target memory space | 0x0040 | R/W
- XTS_AESTINATION_REG | Configures the type of the external memory | 0x0044 | R/W
- ... | ... | ... | ...

**Subsection Title:**
Contro/Status Registers

**List Items (Partial):**

- XTS_AES_TRIGGER_REG | Activates AES algorithm | 0x004C | WO
- XTS_AES_RELEASE_REG | Release control | 0x0050 | WO
- ... | ... | ... | ...

**Subsection Title:**
Version Register

**List Items (Partial):**

- XTS_AES_DATE_REG | Version control register | 0x005C | RO
- ... | ... | ... | ...

**Footer Information:**
Espressif Systems  
915 ESP32-S3 TRM (Version 1.7)  

**Link Texts:**
Submit Documentation Feedback

**Navigation Link:** 
GoBack