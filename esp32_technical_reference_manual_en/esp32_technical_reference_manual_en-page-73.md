**Chapter Title:**
Chapter 3 System and Memory

**Table Header:**
- Bus Type
- Boundary Address (Low Address)
- High Address
- Size
- Target
- Comment

**Table Content:**

| Bus Type | Low Address       | High Address      | Size   | Target    | Comment                          |
|----------|-------------------|--------------------|--------|-----------|----------------------------------|
| Data     | 0x3FF5_4000      | 0x3FF5_4FFF        | 4 KB   | UDMA      |                                 |
| Data     | 0x3FF5_5000      | 0x3FF5_5FFF        | 4 KB   | SDIO Slave| One of three parts               |
| Data     | 0x3FF5_6000      | 0x3FF5_6FFF        | 4 KB   | RMT       |                                 |
| Data     | 0x3FF5_7000      | 0x3FF5_7FFF        | 4 KB   | PCNT      |                                 |
| Data     | 0x3FF5_8000      | 0x3FF5_8FFF        | 4 KB   | SDIO Slave| One of three parts               |
| Data     | 0x3FF5_9000      | 0x3FF5_9FFF        | 4 KB   | LED PWM   |                                 |
| Data     | 0x3FF5_A000      | 0x3FF5_AFFF        | 4 KB   | eFuse     |                                 |
| Data     | 0x3FF5_B000      | 0x3FF5_BFFF        | 4 KB   | Flash Encryption |                      |
| Data     | 0x3FF5_C000      | 0x3FF5_DFFF        | 8 KB   | Reserved  |                                 |
| Data     | 0x3FF5_E000      | 0x3FF5_EFFF        | 4 KB   | MCPWM0    |                                 |
| Data     | 0x3FF5_F000      | 0x3FF5_FFFF        | TIMGO1 |           |                                 |
| Data     | 0x3FF6_0000      | 0x3FF6_0FFF        | 4 KB   | TIMG1     |                                 |
| Data     | 0x3FF6_1000      | 0x3FF6_3FFF        | 12 KB  | Reserved  |                                 |
| Data     | 0x3FF6_4000      | 0x3FF6_4FFF        | 4 KB   | SPI2      |                                 |
| Data     | 0x3FF6_5000      | 0x3FF6_5FFF        | 4 KB   | SPI3      |                                 |
| Data     | 0x3FF6_6000      | 0x3FF6_6FFF        | 4 KB   | SYSCON    |                                 |
| Data     | 0x3FF6_7000      | 0x3FF6_7FFF        | 4 KB   | I2C1      |                                 |
| Data     | 0x3FF6_8000      | 0x3FF6_8FFF        | 4 KB   | SDMMC    |                                 |
| Data     | 0x3FF6_9000      | 0x3FF6_AFFF        | 8 KB   | EMAC     |                                 |
| Data     | 0x3FF6_B000      | 0x3FF6_BFFF        | 4KB    | TWAI      |                                 |
| Data     | 0x3FF6_C000      | 0x3FF6_CFFF        | 4 KB   | MCPWM1    |                                 |
| Data     | 0x3FF6_D000      | 0x3FF6_DFFF        | 4 KB   | I2S1      |                                 |
| Data     | 0x3FF6_E000      | 0x3FF6_FFFF        | 4 KB   | UART2     |                                 |
| Data     | 0x3FF6_F000      | 0x3FF6_FFFF        | Reserved |           |                                 |
| Data     | 0x3FF7_0000      | 0x3FF7_0FFF        | 4 KB   | Reserved  |                                 |
| Data     | 0x3FF7_1000      | 0x3FF7_4FFF        | 16 KB  | Reserved  |                                 |
| Data     | 0x3FF7_5000      | 0x3FF7_5FFF        | 4 KB   | RNG       |                                 |
| Data     | 0x3FF7_6000      | 0x3FF7_FFFF        | 40 KB  | Reserved  |                                 |

**Notice:**
- Peripherals accessed by the CPU via `0x3FF40000 ~ 0x3FF7FFFF` address space (DPORT address) can also be accessed via `0x60000000 ~ 0x6003FFFFF` (AHB address). The `(0x3FF40000 + n)` address and `(0x60000000 + n)` addresses access the same content, where \(n = 0\) to `0x3FFFF`.
- The CPU can access peripherals via DPORT address more efficiently than via AHB address. However, DPOR address is characterized by speculative reads, which means it cannot guarantee that each read is valid. In addition, DPOR address will upset the order of r/w operations on the bus to improve performance, which may cause programs that have strict requirements on the r/w order to crash.

**Additional Information:**
- On the other hand, using AHB address to read FIFO registers will cause unpredictable errors.
- To address above issues please strictly follow the instructions documented in [ESP32 ECO and Workarounds for Bugs](#), specifically sections 3.3, 3.10, 3.16, and 3.17.

**Footer:**
Espressif Systems
Page number: 73
Document version: ESP32 TRM (Version 5.6)
Submit Documentation Feedback