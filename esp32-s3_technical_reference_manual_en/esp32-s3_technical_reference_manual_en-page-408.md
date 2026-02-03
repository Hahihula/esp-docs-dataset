**Chapter Title:**
4.3 System and Memory

**Section Heading:**
4.3.5.1 Module/Peripheral Address Mapping

**Body Text:**
Table 4.3-3 lists all the modules/peripherals and their respective address ranges. Note that the address space of specific modules/peripherals is defined by “Boundary Address” (including both Low Address and High Address).

**Table Title:**
Table 4.3-3. Module/Peripheral Address Mapping

| Target                   | Boundary Address       | Size (KB) | Notes |
|--------------------------|------------------------|-----------|-------|
| UART Controller O        | Low Address: 0x6000_0000, High Address: 0x6000_OFFFF | -         | 4     |
| Reserved                 | Low Address: 0x6000_1000, High Address: 0x6000_1FFF   | -         |       |
| SPI Controller 1         | Low Address: 0x6000_2000, High Address: 0x6000_2FFF   | -         | 4     |
| SPI Controller O         | Low Address: 0x6000_3000, High Address: 0x6000_3FFF   | -         | 4     |
| GPIO                     | Low Address: 0x6000_4000, High Address: 0x6000_4FFF   | -         | 4     |
| Reserved                 | Low Address: 0x6000_5000, High Address: 0x6000_5FFF   | -         |       |
| eFuse Controller         | Low Address: 0x6000_7000, High Address: 0x6000_7FFF   | -         | 4     |
| Low-Power Management     | Low Address: 0x6000_8000, High Address: 0x6000_8FFF   | -         | 4     |
| IO MUX                   | Low Address: 0x6000_9000, High Address: 0x6000_9FFF   | -         | 4     |
| Reserved                 | Low Address: 0x6000_A000, High Address: 0x6000_EFFF   | -         |       |
| I2S Controller O         | Low Address: 0x6000_F000, High Address: 0x6000_FFFF   | -         | 4     |
| UART Controller 1        | Low Address: 0x6001_0000, High Address: 0x6001_OFFFF   | -         | 4     |
| Reserved                 | Low Address: 0x6001_1000, High Address: 0x6001_2FFF   | -         |       |
| I2C Controller O         | Low Address: 0x6001_3000, High Address: 0x6001_3FFF   | -         | 4     |
| UHCIO                    | Low Address: 0x6001_4000, High Address: 0x6001_4FFF   | -         | 4     |
| Reserved                 | Low Address: 0x6001_5000, High Address: 0x6001_5FFF   | -         |       |
| Remote Control Peripheral| Low Address: 0x6001_6000, High Address: 0x6001_6FFF   | -         | 4     |
| Pulse Count Controller   | Low Address: 0x6001_7000, High Address: 0x6001_7FFF   | -         | 4     |
| Reserved                 | Low Address: 0x6001_8000, High Address: 0x6001_8FFF   | -         |       |
| LED PWM Controller       | Low Address: 0x6001_9000, High Address: 0x6001_9FFF   | -         | 4     |
| Reserved                 | Low Address: 0x6001_A000, High Address: 0x6001_DFFF   | -         |       |
| Motor Control PWM O      | Low Address: 0x6001_E000, High Address: 0x6001EFFF     | -         | 4     |
| Timer Group O            | Low Address: 0x6002_0000, High Address: 0x6002_0FFF   | -         |       |
| Timer Group 1            | Low Address: 0x6002_1000, High Address: 0x6002_2FFF   | -         | 8     |
| RTC SLOW Memory          | Low Address: 0x6002_3000, High Address: 0x6002_3FFF   | -         |       |
| System Timer             | Low Address: 0x6002_4000, High Address: 0x6002_4FFF   | -         | 4     |
| SPI Controller 2         | Low Address: 0x6002_5000, High Address: 0x6002_5FFF   | -         |       |
| I2C Controller 3         | Low Address: 0x6002_6000, High Address: 0x6002_6FFF   | -         | 4     |
| SYSCON                   | Low Address: 0x6002_7000, High Address: 0x6002_7FFF   | -         |       |
| SD/MMC Host Controller   | Low Address: 0x6002_8000, High Address: 0x6002_8FFF   | -         | 4     |
| Reserved                 | Low Address: 0x6002_9000, High Address: 0x6002_AFFF   | -         |       |
| Two-wire Automotive Interface | Low Address: 0x6002_B000, High Address: 0x6002_BFFF | -         | 4     |
| Motor Control PWM 1      | Low Address: 0x6002_C000, High Address: 0x6002_CFFF   | -         |       |
| I2S Controller 1         | Low Address: 0x6002_D000, High Address: 0x6002_DFFF   | -         |       |

**Footer Text:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version Information:**
408 ESP32-S3 TRM (Version 1.7)