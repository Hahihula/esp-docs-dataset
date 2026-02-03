**Chapter Title:**
Chapter 19 AES Accelerator (AES)

**Section Heading:**
19.7 Register Summary

**Body Text:**
The addresses in this section are relative to the AES accelerator base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table Headers:**
- Name
- Description
- Address
- Access

**Table Content (Partial):**

| Key Registers | AES_KEY_0_REG | AES key register 0 | 0x0000 | R/W |
| --- | --- | --- | --- | --- |
| | AES_KEY_1_REG | AES key register 1 | 0x0004 | R/W |
| | AES_KEY_2_REG | AES key register 2 | 0x0008 | R/W |
| | AES_KEY_3_REG | AES key register 3 | 0x000C | R/W |
| | AES_KEY_4_REG | AES key register 4 | 0x0010 | R/W |
| | AES_KEY_5_REG | AES key register 5 | 0x0014 | R/W |
| | AES_KEY_6_REG | AES key register 6 | 0x0018 | R/W |
| | AES_KEY_7_REG | AES key register 7 | 0x001C | R/W |

**Subsection Titles and Descriptions:**

- TEXT_IN Registers
  - AES_TEXT_IN_0_REG | Source data register 0 | Address: 0x0020, Access: R/W
  - AES_TEXT_IN_1_REG | Source data register 1 | Address: 0x0024, Access: R/W

- TEXT_OUT Registers
  - AES_TEXT_OUT_0_REG | Result data register 0 | Address: 0x0030, Access: RO (Read Only)
  - AES_TEXT_OUT_1_REG | Result data register 1 | Address: 0x0034, Access: RO

- Configuration Registers
  - AES_MODE_REG | Defines key length and encryption/decryption mode. Selects the working mode of the AES accelerator or defines the block cipher mode | Address: 0x0040, Access: R/W (Read/Write)
  - AES_DMA_ENABLE_REG | Standard incrementing function register | Address: 0x0090, Access: R/W

- Controlling/Status Registers
  - AES_TRIGGER_REG | Operation start controlling register | Address: 0x0048, Access: WO (Write Only)
  - AES_STATE_REG | Operation status register | Address: 0x004C, Access: RO (Read Only)

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Type:**
ESP32-S3 TRM (Version 1.7)