**Chapter Title:**
Chapter 3 System and Memory

**Body Text:**
ESP32 Cache supports the Flush function. It is worth noting that when the Flush function is used, the data written in the cache will be disposed rather than being rewritten into the External SRAM. To enable the Flush function, first clear bit `x_CACHE_FLUSH_ENA` in register `DPORT_x_CACHETRL_REG`, then set this bit to 1. Afterwards, the system hardware will set bit `x_CACHE_FLUSH_DONE` to 1, where `x` can be "PRO" or "APP", indicating that the cache flush operation has been completed.

For more information about the address mapping of ESP32 Cache, please refer to [Embedded Memory](#) and [External Memory](#).

**Subsection Title:**
3.3.5 Peripherals

**Body Text:**
The ESP32 has 41 peripherals. Table **3.3-6** specifically describes the peripherals and their respective address ranges. Nearly all peripheral modules can be accessed by either CPU at the same address with just a single exception; this being the PID Controller.

**Table Title:**
Table 3.3-6. Peripheral Address Mapping

| Bus Type | Boundary Address       | Size    | Target                   | Comment                                    |
|----------|------------------------|---------|--------------------------|--------------------------------------------|
| Data     | Low Address            | High Address   |                           |                                            |
|          | `0x3FF0_0000`         | `0x3FF0_OFFF`  | 4 KB                     | DPort Register                             |
|          | `0x3FF0_1000`         | `0x3FF0_1FFF`  | 4 KB                     | AES Accelerator                            |
|          | `0x3FF0_2000`         | `0x3FF0_2FFF`  | 4 KB                     | RSA Accelerator                             |
|          | `0x3FF0_3000`         | `0x3FF0_3FFF`  | 4 KB                     | SHA Accelerator                            |
|          | `0x3FF0_4000`         | `0x3FF0_4FFF`  | 4 KB                     | Secure Boot                               |
|          | `0x3FF0_5000`         | `0x3FF0_FFFF`  | 44 KB                    | Reserved                                  |
|          | `0x3FF1_0000`         | `0x3FF1_EFFF`  | 16 KB                    | Cache MMU Table                             |
|          | `0x3FF1_4000`         | `0x3FF1_FFFF`  | 44 KB                    | Reserved                                  |
|          | `0x3FF1_F000`         | `0x3FF1_FFFF`  | 4 KB                     | PID Controller                             |
| Data     |                        | Per-CPU peripheral|
|          | `0x3FF2_0000`         | `0x3FF3_FFFF`  | 128 KB                   | Reserved                                  |
|          | `0x3FF4_0000`         | `0x3FF4_FFFF`  | 4 KB                     | UART0                                      |
|          | `0x3FF4_1000`         | `0x3FF4_FFFF`  | 4 KB                     | Reserved                                  |
| Data     |                        | SPI1                                   |
|          | `0x3FF4_2000`         | `0x3FF4_3FFF`  | 4 KB                     | SPI0                                      |
|          | `0x3FF4_4000`         | `0x3FF4_4FFF`  | 4 KB                     | GPIO                                      |
| Data     |                        | Reserved                               |
|          | `0x3FF4_5000`         | `0x3FF4_7FFF`  | 12 KB                    | Reserved                                  |
|          | `0x3FF4_8000`         | `0x3FF4_8FFF`  | 4 KB                     | RTC                                        |
| Data     |                        | IO MUX                                   |
|          | `0x3FF4_A000`         | `0x3FF4_AFFF`  | 4 KB                     | Reserved                                  |
|          | `0x3FF4_B000`         | `0x3FF4_BFFF`  | 4 KB                     | SDIO Slave                                |
| Data     |                        | One of three parts                      |
|          | `0x3FF4_C000`         | `0x3FF4_CFFF`  | 4 KB                     | UDMA1                                      |
|          | `0x3FF4_D000`         | `0x3FF4_FFFF`  | 8 KB                     | Reserved                                  |
| Data     |                        | I2S0                                     |
|          | `0x3FF5_0000`         | `0x3FF5_FFFF`  | 4 KB                     | UART1                                      |
|          | `0x3FF5_1000`         | `0x3FF5_2FFF`  | 8 KB                     | Reserved                                  |
| Data     |                        | I2C0                                     |

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)