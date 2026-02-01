**Title: Functional Description**

- **ESP32-H2FH2S chip variant:** 2 MB
- ESP32-H2FH4S chip variant: 4 MB

- More than 100,000 program/erase cycles
- More than 20 years of data retention time

- Clock frequency:
  - ESP32-H2FH2S chip variant: up to 64 MHz
  - ESP32-H2FH4S chip variant: up to 64 MHz

For details, see [ESP32-H2 Technical Reference Manual > Chapter System and Memory](#).

---

**Subtitle: External Memory (Section 4.1.2.2)**

ESP32-H2 allows connection to memories outside the chip's package via the SPI, Dual SPI, Quad SPI, and QPI interfaces.

- **Feature List**
  - Support connection to off-package flash of 16 MB at most
    - Support hardware encryption/decryption based on XTS-AES
  - Up to 16 MB of CPU instruction memory space can map into flash as individual blocks of 64 KB. 32-bit fetch is supported
  - Up to 16 MB of CPU data memory space can map into flash as individual blocks of 64 KB. 8-bit, 16-bit and 32-bit reads are supported

- External memory accessed via a 16 KB read-only cache:
  - Eight-way set associative
  - 32-byte cache block
  - Critical word first and early restart

For details, see [ESP32-H2 Technical Reference Manual > Chapter System and Memory](#).

---

**Subtitle: eFuse Controller (Section 4.1.2.3)**

The eFuse memory is a one-time programmable memory that stores parameters and user data. The eFuse controller in the ESP32-H2 is responsible for programming and reading this memory.

- **Feature List**
  - Configurable write protection for some blocks
  - Configurable read protection for some blocks
  - Various hardware encoding schemes against data corruption

For details, see [ESP32-H2 Technical Reference Manual > Chapter eFuse Controller](#).

---

**Footer:**

Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32-H2 Series Datasheet v1.2