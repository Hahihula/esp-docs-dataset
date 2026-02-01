**Title: Functional Description**

- More than 20 years of data retention time
- Clock frequency up to 120 MHz

**Subtitle: In-package PSRAM**
- See PSRAM size in Chapter 1 ESP32-C61 Series Comparison
- Clock frequency up to 120 MHz

---

**Title: External Memory (4.1.2.2)**

Some variants of ESP32-C61 allow connection to flash/PSRAM via the SPI, Dual SPI, Quad SPI, and QPI interfaces. For more information, please refer to Table 1-1.

CPU’s instruction memory space and read-only data memory space can map into the flash/PSRAM of ESP32-C61, and the size of the flash/PSRAM can be 32 MB at most respectively. ESP32-C61 supports hardware encryption/decryption based on XTS-AES to protect developers’ programs and data in the flash/PSRAM.

**Subtitle: Feature List**

Through the cache, ESP32-C61 can support at a time up to:

- 32 MB of instruction memory space which can map into the flash/PSRAM as individual blocks of 64/32/16 KB. 32-bit fetch is supported
- 32 MB of data memory space which can map into the flash/PSRAM as individual blocks of 64/32/16 KB.
8-bit, 16-bit, and 32-bit reads are supported by the flash. 8-bit, 16-bit, and 32-bit reads and writes are supported by the PSRAM

**Note:**
After ESP32-C61 is initialized, software can customize the mapping of flash/PSRAM into the CPU address space.

---

**Title: eFuse Controller (4.1.2.3)**

The eFuse memory is a one-time programmable memory that stores parameters and user data, and the eFuse controller of ESP32-C61 is used to program and read this eFuse memory.

**Subtitle: Feature List**

- Configure write protection for some blocks
- Configure read protection for some blocks
- Various hardware encoding schemes against data corruption

---

**Title: System Components (4.1.3)**

This subsection describes the essential components that contribute to the overall functionality and control of the system.

Espressif Systems  
Page 34 ESP32-C61 Series Datasheet v0.5