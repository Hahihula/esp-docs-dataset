**Chapter Title:**
Chapter 21 HMAC Accelerator (HMAC)

**Section Header:**
21.4 Register Summary

**Body Text:**
The addresses in this section are relative to HMAC Accelerator base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Headers:**
- Name
- Status/Control Register Description
- Address
- Access

**Table Content (Partial):**

| Name | Status/Control Register Description | Address | Access |
|------|---------------------------------------|---------|--------|
| HMAC_SET_START_REG | HMAC start control register | 0x040 | WO |
| HMAC_SET_PARA PURPOSE_REG | HMAC parameter purpose register | 0x044 | WO |
| ... | ... | ... | ... |

**Subsection Title:**
HMAC Message Block

**Table Content (Partial):**

| Name | Status/Control Register Description | Address | Access |
|------|---------------------------------------|---------|--------|
| HMAC_WR_MESSAGE_0_REG | Message register 0 | 0x080 | WO |
| HMAC_WR_MESSAGE_1_REG | Message register 1 | 0x084 | WO |
| ... | ... | ... | ... |

**Subsection Title:**
HMAC Upstream Result

**Table Content (Partial):**

| Name | Status/Control Register Description | Address | Access |
|------|---------------------------------------|---------|--------|
| HMAC_RD_RESULT_0_REG | Hash result register 0 | 0x0C0 | RO |
| HMAC_RD_RESULT_1_REG | Hash result register 1 | 0x0C4 | RO |
| ... | ... | ... | ... |

**Footer:**
Espressif Systems  
890 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback