**Title: Functional Description**

---

### **4.1.2.1 Internal Memory**

The internal memory of ESP32-S3 refers to the memory integrated on the chip die or in the chip package, including ROM, SRAM, eFuse, and flash.

#### Feature List

- 384 KB ROM: for booting and core functions
- 512 KB on-chip SRAM: for data and instructions, running at a configurable frequency of up to 240 MHz
- RTC FAST memory: 8 KB SRAM that supports read/write/instruction fetch by the main CPU (LX7 dual-core processor). It can retain data in Deep-sleep mode
- RTC SLOW Memory: 8 KB SRAM that supports read/write/instruction fetch by the main CPU (LX7 dual-core processor) or coprocessors. It can retain data in Deep-sleep mode
- 4096-bit eFuse memory: 1792 bits are available for users, such as encryption key and device ID. See also Section **4.1.2.4 eFuse Controller**

#### In-package flash and PSRAM:

- [See flash and PSRAM size in Chapter 1 ESP32-S3 Series Comparison](#)
- For specifications, refer to Section *5.7 Memory Specifications*.

For details, see **ESP32-S3 Technical Reference Manual > Chapter System and Memory**.

---

### **4.1.2.2 External Flash and RAM**

ESP32-S3 supports SPI, Dual SPI, Quad SPI, Octal SPI, QPI, and OPI interfaces that allow connection to multiple external flash and RAM.
The external flash and RAM can be mapped into the CPU instruction memory space and read-only data memory space. The external RAM can also be mapped into the CPU data memory space. ESP32-S3 supports up to 1 GB of external flash and RAM, and hardware encryption/decryption based on XTS-AES to protect users’ programs and data in flash and external RAM.

Through high-speed caches, ESP32-S3 can support at a time up to:
- External flash or RAM mapped into 32 MB instruction space as individual blocks of 64 KB
- External RAM mapped into 32 MB data space as individual blocks of 64 KB. 8-bit, 16-bit, 32-bit, and 128-bit reads and writes are supported. External flash can also be mapped into 32 MB data space as individual blocks of 64 KB, but only supporting 8-bit, 16-bit, 32-bit and 128-bit reads.

**Note:** After ESP32-S3 is initialized, firmware can customize the mapping of external RAM or flash into the CPU address space.
For details, see **ESP32-S3 Technical Reference Manual > Chapter System and Memory**.

---

### **4.1.2.3 Cache**

ESP32-S3 has an instruction cache and a data cache shared by the two CPU cores. Each cache can be partitioned into multiple banks.

Espressif Systems

Page 39
[Submit Documentation Feedback](#)