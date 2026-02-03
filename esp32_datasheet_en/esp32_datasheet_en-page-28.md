**Title: Functional Description**

---

**Table Title:** Table 4-1. Memory and Peripheral Mapping

| Category       | Target                   | Start Address    | End Address     | Size   |
|----------------|--------------------------|------------------|-----------------|--------|
| Embedded Memory |                           |                   |                 |        |
| - Internal ROM0 |                           | 0x4000_0000      | 0x4005_FFFF    | 384 KB |
| - Internal ROM1 |                           | 0x3FF9_0000      | 0x3FF9_FFFF    | 64 KB  |
| - Internal SRAM0 |                          | 0x4007_0000      | 0x4009_FFFF    | 192 KB |
| - Internal SRAM1 |                          | 0x3FFE0_0000      | 0x3FFF_FFFF    | 128 KB |
|                  | Internal SRAM 2          | 0x40A0_0000      | 0x40B_FFFF     |        |
| - RTC FAST Memory |                      | 0x3FF8_0000      | 0x3FFD_FFFF    | 200 KB |
|                  |                          |                   |                 |        |
| External Memory |                           |                   |                 |        |
| - External Flash |                          | 0x400C_0000      | 0x407F_FFFF    | 8 KB   |
| - External RAM1  |                          | 0x3FFA_0000      | 0x3FFD_FFFF    |        |
|                  |                          |                   |                 |        |
| Peripheral       |                           |                   |                 |        |
| - DPort Register |                          | 0x3FF0_0000      | 0x3FFF_FFFF    | 4 KB   |
| - AES Accelerator |                        | 0x3FF1_0000      | 0x3FFF_FFFF    |        |
| - RSA Accelerator |                        | 0x3FF2_0000      | 0x3FFF_FFFF    |        |
| - SHA Accelerator |                       | 0x3FF3_0000      | 0x3FFF_FFFF    |        |
| - Secure Boot   |                          | 0x3FF4_0000      | 0x3FFF_FFFF    |        |
| - Cache MMU Table|                        | 0x3FF5_0000      | 0x3FFD_FFFF    | 16 KB  |
| - PID Controller |                       | 0x3FF6_0000      | 0x3FFD_FFFF    |        |
| - UART0          |                          | 0x3FF7_0000      | 0x3FFD_FFFF    |        |
| - SPI1           |                          | 0x3FF8_0000      | 0x3FFD_FFFF    |        |
| - SPI0           |                          | 0x3FF9_0000      | 0x3FFD_FFFF    |        |
| - GPIO           |                          | 0x3FFA_0000      | 0x3FFD_FFFF    |        |
| - RTC            |                          | 0x3FFB_0000      | 0x3FFD_FFFF    |        |
| - IO MUX         |                          | 0x3FFC_0000      | 0x3FFD_FFFF    |        |
| - SDIO Slave     |                          | 0x3FFD_0000      | 0x3FFD_FFFF    |        |
| - UDMA1          |                          | 0x3FFE_0000      | 0x3FFD_FFFF    |        |
| - I2SO           |                          | 0x3FFF_0000      | 0x3FFD_FFFF    |        |
| - UART1          |                          | 0x3FF5_0000      | 0x3FFD_FFFF    |        |
| - I2CO           |                          | 0x3FF6_0000      | 0x3FFD_FFFF    |        |
| - UDMA0          |                          | 0x3FF7_0000      | 0x3FFD_FFFF    |        |
| - SDIO Slave     |                          | 0x3FF8_0000      | 0x3FFD_FFFF    |        |
| - RMT            |                          | 0x3FF9_0000      | 0x3FFD_FFFF    |        |
| - PCNT           |                          | 0x3FFA_0000      | 0x3FFD_FFFF    |        |
| - SDIO Slave     |                          | 0x3FFB_0000      | 0x3FFD_FFFF    |        |
| - LED PWM         |                         | 0x3FFC_0000      | 0x3FFD_FFFF    |        |
| - eFuse Controller|                      | 0x3FFD_0000      | 0x3FFD_FFFF    |        |
| - Flash Encryption|                       | 0x3FFE_0000      | 0x3FFD_FFFF    |        |
| - PWMO           |                          | 0x3FFF_0000      | 0x3FFD_FFFF    |        |
| - TIMGO          |                          | 0x3FF5_0000      | 0x3FFD_FFFF    |        |
| - TIMG1          |                          | 0x3FF6_0000      | 0x3FFD_FFFF    |        |
| - SPI2           |                          | 0x3FF7_0000      | 0x3FFD_FFFF    |        |
| - SPI3           |                          | 0x3FF8_0000      | 0x3FFD_FFFF    |        |

---

**Footer:**
Espressif Systems
ESP32 Series Datasheet v5.2

Submit Documentation Feedback