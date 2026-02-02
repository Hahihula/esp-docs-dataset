**Chapter Title:**
Chapter 16 SHA Accelerator (SHA)

**Table of Registers and Their Descriptions**

| Name                          | Description                                                                                   | Address     | Access |
|-------------------------------|----------------------------------------------------------------------------------------------|-------------|--------|
| SHA_SHA1_LOAD_REG            | Control register to calculate the final SHA1 hash                                             | 0x3FF03088 | WO     |
| SHA_SHA1 BUSY_REG            | Status register for SHA1 operation                                                            | 0x3FF0308C | RO     |
| SHA_SHA256_START_REG         | Control register to initiate SHA256 operation                                                | 0x3FF03090 | WO     |
| SHA_SHA256_CONTINUE_REG      | Control register to continue SHA256 operation                                                | 0x3FF03094 | WO     |
| SHA_SHA256_LOAD_REG          | Control register to calculate the final SHA256 hash                                          | 0x3FF03098 | WO     |
| SHA_SHA256 BUSY_REG          | Status register for SHA256 operation                                                          | 0x3FF0309C | RO     |
| SHA_SHA384_START_REG         | Control register to initiate SHA384 operation                                                | 0x3FF030A0 | WO     |
| SHA_SHA384_CONTINUE_REG      | Control register to continue SHA384 operation                                                | 0x3FF030A4 | RO     |
| SHA_SHA384_LOAD_REG          | Control register to calculate the final SHA384 hash                                          | 0x3FF030A8 | WO     |
| SHA_SHA384 BUSY_REG          | Status register for SHA384 operation                                                          | 0x3FF030AC | RO     |
| SHA_SHA512_START_REG         | Control register to initiate SHA512 operation                                                | 0x3FF030B0 | WO     |
| SHA_SHA512_CONTINUE_REG      | Control register to continue SHA512 operation                                                | 0x3FF030B4 | RO     |
| SHA_SHA512_LOAD_REG          | Control register to calculate the final SHA512 hash                                          | 0x3FF030B8 | WO     |
| SHA_SHA512 BUSY_REG          | Status register for SHA512 operation                                                          | 0x3FF030BC | RO     |

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)