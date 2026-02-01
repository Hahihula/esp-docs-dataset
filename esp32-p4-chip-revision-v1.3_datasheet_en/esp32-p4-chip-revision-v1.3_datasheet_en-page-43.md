**Title: Functional Description**

---

### In-package PSRAM

- The size of PSRAM is detailed in Section **1 ESP32-P4 Series Comparison**
- Maximum clock frequency: 200 MHz
- Supports up to 64 MB storage
- Supports hardware XTS-AES encryption/decryption, protecting programs and data stored in PSRAM through a cache; it can map 64 KB blocks into a 64 MB instruction or data space, supporting 8-bit, 16-bit, 32-bit, and 128-bit read and write operations

---

### External Memory

ESP32-P4 allows connection to memories outside the chip's package via the SPI, Dual SPI, Quad SPI, and QPI interfaces. The maximum clock frequency is 120 MHz.

The external flash can be mapped into the CPU instruction memory space and read-only data memory space. ESP32-P4 supports up to 64 MB of external flash, and hardware encryption/decryption based on XTS-AES to protect users' programs and data in flash through high-speed caches; ESP32-P4 can support at a time:

- External flash mapped into 64 MB instruction space as individual blocks of 64 KB
- External flash can also be mapped into 64 MB data space as individual blocks of 64 KB, supporting 8-bit, 16-bit, 32-bit, and 128-bit reads.

**Note:** After ESP32-P4 is initialized, firmware can customize the mapping of external flash into the CPU address space

---

### eFuse Controller (Section **4.1.3.2**)

ESP32-P4 contains a 4096-bit eFuse memory to store parameters and user data. The parameters include control parameters for some hardware modules, system data parameters, and keys used for encryption/decryption module.

Once an eFuse bit is programmed to 1, it can never be reverted to 0

**Feature List:**
- 4096-bit one-time programmable memory (including up to 1792 bits reserved for custom use)
- Configurable write protection
- Configurable read protection
- Various hardware encoding schemes against data corruption

---

### Cache (Section **4.1.3.3**)

ESP32-P4 employs the two-level cache structure.

---

*Espressif Systems*
*Submit Documentation Feedback*

**Page Number:** 43  
**Document Title:** ESP32-P4 Series Datasheet v0.6