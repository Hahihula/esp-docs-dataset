**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**Section Titles and Content:**

1. **18.4.4 Interrupt**
   - Description:
     "SHA accelerator supports interrupt on the completion of message digest calculation when working in the DMA-SHA mode. To enable this function, write 1 to register SHA_INT_ENA_REG. Note that the interrupt should be cleared by software after use via setting the SHA_INT_CLEAR_REG register to 1."

2. **18.5 Register Summary**
   - Introduction:
     "The addresses in this section are relative to the SHA accelerator base address provided in Table 4.3-3 in Chapter 4 System and Memory."
   - Note about abbreviations: 
     "The abbreviations given in Column Access are explained in Section Access Types for Registers."

**Table Content (with headers):**

| Name                          | Description                                                                                   | Address       | Access |
|-------------------------------|----------------------------------------------------------------------------------------------|---------------|--------|
| Control/Status registers     |                                                                                               |               |        |
| SHA_CONTINUE_REG             | Continues SHA operation (only effective in Typical SHA mode)                                  | 0x0014        | WO     |
| SHA BUSY_REG                 | Indicates if SHA Accelerator is busy or not                                                   | 0x0018        | RO     |
| SHA_DMA_START_REG            | Starts the SHA accelerator for DMA-SHA operation                                               | 0x001C        | WO     |
| SHA_START_REG                | Starts the SHA accelerator for Typical SHA operation                                           | 0x0010        | WO     |
| SHA_DMA_CONTINUE_REG         | Continues SHA operation (only effective in DMA-SHA mode)                                     | 0x0020        | WO     |
| SHA_INT_CLEAR_REG            | DMA-SHA interrupt clear register                                                             | 0x0024        | WO     |
| SHA_INT_ENA_REG              | DMA-SHA interrupt enable register                                                            | 0x0028        | R/W    |
| Version Register              |                                                                                               |               |        |
| SHA_DATE_REG                 | Version control register                                                                      | 0x002C        | R/W    |
| Configuration Registers       |                                                                                               |               |        |
| SHA_MODE_REG                  | Defines the algorithm of SHA accelerator                                                     | 0x0000        | R/W    |
| SHA_T_STRING_REG             | String content register for calculating initial Hash Value (only effective for SHA-512/t)   | 0x0004        | R/W    |
| SHA_T_LENGTH_REG             | String length register for calculating initial Hash Value (only effective for SHA-512/t)     | 0x0008        | R/W    |
| Memories                      |                                                                                               |               |        |
| SHA_DMA_BLOCK_NUM_REG        | Block number register (only effective for DMA-SHA)                                          | 0x00C         | R/W    |
| SHA_H_0_REG                   | Hash value                                                                                    | 0x040         | R/W    |
| SHA_H_1_REG                   | Hash value                                                                                    | 0x044         | R/W    |
| SHA_H_2_REG                   | Hash value                                                                                    | 0x048         | R/W    |
| SHA_H_3_REG                   | Hash value                                                                                    | 0x04C         | R/W    |
| SHA_H_4_REG                   | Hash value                                                                                    | 0x050         | R/W    |
| SHA_H_5_REG                   | Hash value                                                                                    | 0x054         | R/W    |
| SHA_H_6_REG                   | Hash value                                                                                    | 0x058         | R/W    |
| SHA_H_7_REG                   | Hash value                                                                                    | 0x05C         | R/W    |

**Footer:**
- Company Name: Espressif Systems
- Document Version and Type Information:
  - "ESP32-S3 TRM (Version 1.7)"
  - Page Number: 852

**Navigation Links:**
- GoBack button at the top right corner.

**Note:** The table is structured to provide a clear overview of different registers, their functions, addresses in hexadecimal format and access types for programming purposes related to SHA accelerator operations on ESP32-S3 microcontroller.