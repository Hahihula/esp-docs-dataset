**Title: Functional Description**

---

### **4.1.2 Internal Memory**

The internal memory of ESP32-C5 refers to the memory integrated on the chip die or in the chip package, including ROM, SRAM, eFuse, and flash.

#### Feature List

- 320 KB of ROM for booting and core functions
- 384 KB of SRAM for data and instructions
- 16 KB of low-power SRAM (LP SRAM) that can be accessed by HP CPU or LP CPU. It can retain data in Deep-sleep mode
- 4 Kbit of eFuse memory, with 1792 bits available for users

For details, see [ESP32-C5 Technical Reference Manual > Chapter System and Memory](#).

---

### **4.1.2.2 External Memory**

ESP32-C5 supports SPI, Dual SPI, Quad SPI, and QPI interfaces that allow connection to the external flash and PSRAM.

CPU’s instruction memory space and read-only data memory space can map into the external flash and PSRAM of ESP32-C5, and the size of the external flash or PSRAM can be 32 MB at most. ESP32-C5 supports hardware encryption/decryption based on XTS-AES to protect developers’ programs and data in the external flash and PSRAM.

#### Feature List

- 32 MB of instruction memory space which can map into the external flash and PSRAM as individual blocks of 64 KB, 32-bit fetch is supported
- 32 MB of data memory space which can map into the external flash and PSRAM as individual blocks of 64 KB. 8-bit, 16-bit, and 32-bit reads are supported by the external flash.
- 8-bit, 16-bit, and 32-bit writes are supported by the external PSRAM

**Note:**
After ESP32-C5 is initialized, software can customize the mapping of off-package flash and PSRAM into the CPU address space.

For details, see [ESP32-C5 Technical Reference Manual > Chapter System and Memory](#).

---

### **4.1.2.3 eFuse Controller**

The eFuse memory is a one-time programmable memory that stores parameters and user data, and the eFuse controller of ESP32-C5 is used to program and read this eFuse memory.

#### Feature List

- 4 Kbits in total, with 1792 bits reserved for users, e.g., encryption key and device ID

---

Espressif Systems  
**Page Number:** 37  
[Submit Documentation Feedback](#)  

ESP32-C5 Series Datasheet v1.0