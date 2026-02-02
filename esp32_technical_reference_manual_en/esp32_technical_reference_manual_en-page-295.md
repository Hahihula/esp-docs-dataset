**Chapter Title:**
Chapter 16 SHA Accelerator (SHA)

**Section Title:**
16.4 Register Summary

**Body Text:**
The addresses in this section are relative to the SHA Accelerator base address provided in Table 3.3-6 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Headers:**
- Name
- Description
- Address
- Access

**Table Content (Partial):**

| Name                          | Description                                                                                   | Address         | Access |
|-------------------------------|----------------------------------------------------------------------------------------------|------------------|--------|
| SHA_TEXT_0_REG               | SHA encrypted/decrypted data register 0                                                     | 0x3FF03000       | R/W    |
| SHA_TEXT_1_REG               | SHA encrypted/decrypted data register 1                                                      | 0x3FF03004       | R/W    |
| ...                          | ...                                                                                           | ...              | ...    |
| SHA_TEXT_25_REG              | SHA encrypted/decrypted data register 25                                                    | 0x3FF06064       | R/W    |
| SHA_TEXT_26_REG              | SHA encrypted/decrypted data register 26                                                    | 0x3FF06068       | R/W    |
| ...                          | ...                                                                                           | ...              | ...    |
| SHA_TEXT_29_REG              | SHA encrypted/decrypted data register 29                                                    | 0x3FF07074       | R/W    |
| SHA_TEXT_30_REG              | SHA encrypted/decrypted data register 30                                                    | 0x3FF07078       | R/W    |
| ...                          | ...                                                                                           | ...              | ...    |
| SHA_TEXT_31_REG              | SHA encrypted/decrypted data register 31                                                    | 0x3FF0707C       | R/W    |

**Subsection Title:**
Control/status registers

**Table Content (Partial):**

| Name                          | Description                                                                                   | Address         | Access |
|-------------------------------|----------------------------------------------------------------------------------------------|------------------|--------|
| SHA_SHA1_START_REG           | Control register to initiate SHA1 operation                                                  | 0x3FF08080       | WO     |
| SHA_SHA1_CONTINUE_REG        | Control register to continue SHA1 operation                                                  | 0x3FF08084       | WO     |

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback