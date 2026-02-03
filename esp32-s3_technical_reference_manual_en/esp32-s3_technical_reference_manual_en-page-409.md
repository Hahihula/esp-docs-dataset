**Chapter Title:**
Chapter 4 System and Memory

**Table Header:**
- Target
- Boundary Address (Low Address)
- High Address
- Size (KB)
- Notes

**Table Content:**

| Target                                 | Low Address       | High Address    | Size (KB) | Notes |
|-----------------------------------------|-------------------|------------------|-----------|-------|
| UART controller 2                      | 0x6002_E000       | 0x6002EFF        | 4         |       |
| Reserved                                | 0x6002_F000       |                  |           |       |
| USB Serial/JTAG Controller             | 0x6003_8000       | 0x6003_8FFF      | 4         |       |
| USB External Control registers         | 0x6003_9000       | 0x6003_9FFF      | 4         | 1     |
| AES Accelerator                         | 0x6003_A000       | 0x6003AFF        | 4         |       |
| SHA Accelerator                         | 0x6003_B000       | 0x6003_BFFF      | 4         |       |
| RSA Accelerator                         | 0x6003_C000       | 0x6003_CFFF      | 4         |       |
| Digital Signature                       | 0x6003_D000       | 0x6003_DFFF      | 4         |       |
| HMAC Accelerator                        | 0x6003_E000       | 0x6003EFF        | 4         |       |
| GDMA Controller                         | 0x6003_F000       | 0x6003FFF        | 4         |       |
| ADC Controller                          | 0x6004_0000       | 0x6004_0FFF      | 4         |       |
| Camera-LCD Controller                   | 0x6004_1000       | 0x6004_1FFF      | 4         |       |
| Reserved                                | 0x6004_2000       |                  |           |       |
| USB core registers                      | 0x6008_0000       | 0x600B_FFFF      | 256       | 1     |
| System Registers                         | 0x600C_0000       | 0x600C_0FFF      | 4         |       |
| PMS Registers                           | 0x600C_1000       | 0x600C_1FFF      | 4         |       |
| Interrupt Matrix                        | 0x600C_2000       | 0x600C_2FFF      | 4         |       |
| Reserved                                | 0x600C_3000       |                  |           |       |
| Reserved                                | 0x600C_4000       | 0x600C_BFFF      |           |       |
| External Memory Encryption and         |                   |                  |           |       |
| Decryption                              | 0x600C_C000       | 0x600C_CFFF      | 4         |       |
| Reserved                                | 0x600D_0000       | 0x600D_DFFF      |           |       |
| Reserved                                | 0x600E_0000       |                  |           |       |
| Reserved                                | 0x600F_0000       | 0x600F_FFFF      |           |       |
| World Controller                        | 0x600D_0000       | 0x600D_DFFF      | 4         |       |

**Notes:**
1. The address space in this module/peripheral is not continuous.
2. The CPU needs to obtain the access permission to a certain module/peripheral when initiating a request to access it, otherwise it may fail. For more information of permission control, please see Chapter **15 Permission Control (PMS)**.

**Footer:**
Espressif Systems
409 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback