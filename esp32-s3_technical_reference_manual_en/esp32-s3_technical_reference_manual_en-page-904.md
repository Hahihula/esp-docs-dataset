**Title:**
Chapter 22 Digital Signature (DS)

**Subtitle:**
22.5 Register Summary

**Body Text:**
The addresses in this section are relative to the Digital Signature base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Headers:**
- Name
- Description
- Address
- Access

**Table Content:**

| **Name**                   | **Description**                                                                                                 | **Address**    | **Access** |
|----------------------------|------------------------------------------------------------------------------------------------------------------|----------------|------------|
| Configuration Registers    |                                                                                                                  |                 |            |
| DS_IV_0_REG               | IV block data                                                                                                   | 0x0630        | WO         |
| DS_IV_1_REG               | IV block data                                                                                                   | 0x0634        | WO         |
| DS_IV_2_REG               | IV block data                                                                                                   | 0x0638        | WO         |
| DS_IV_3_REG               | IV block data                                                                                                   | 0x063C        | WO         |
| Status/Control Registers   |                                                                                                                  |                 |            |
| DS_SET_START_REG          | Activates the DS peripheral                                                                                    | 0xE00         | WO         |
| DS_SET_ME_REG             | Starts DS operation                                                                                             | 0xE04         | WO         |
| DS_SET_FINISH_REG         | Ends DS operation                                                                                                | 0xE08         | WO         |
| DS_QUERY BUSY_REG         | Status of the DS peripheral                                                                                    | 0xE0C         | RO         |
| DS_QUERY_KEY WRONG_REG    | Checks the reason why DS_KEY is not ready                                                                       | 0xE10         | RO         |
| DS_QUERY_CHECK_REG        | Queries DS check result                                                                                         | 0x814         | RO         |
| Version Register           |                                                                                                                  |                 |            |
| DS_DATE_REG                | Version control register                                                                                        | 0x820         | W/R        |

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)