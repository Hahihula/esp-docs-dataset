**Title: Functional Description**

---

### **4.1.2.1 Internal Memory**

The internal memory of ESP32-C6 refers to the memory integrated on the chip die or in the chip package, including ROM, SRAM, eFuse, and flash.

#### Feature List

- 320 KB of ROM for booting and core functions
- 512 KB of high-performance SRAM (HP SRAM) for data and instructions
- 16 KB of low-power SRAM (LP SRAM) that can be accessed by HP CPU or LP CPU. It can retain data in Deep-sleep mode
- 4096-bit eFuse memory, with 1792 bits available for users. See also Section **4.1.2.3 eFuse Controller**
- In-package flash

**See: Chapter ESP32-C6 Series Comparison**

For specifications, refer to Section *5.7 Memory Specifications*.

For details, see [ESP32-C6 Technical Reference Manual > Chapter System and Memory](#).

---

### **4.1.2.2 External Memory**

ESP32-C6 allows connection to memories outside the chip's package via the SPI, Dual SPI, Quad SPI, and QPI interfaces.

#### Feature List

- Support connection to off-package flash of 16 MB at most
  - Support hardware encryption/decryption based on XTS-AES
  - Up to 16 MB of CPU instruction memory space can map into flash as individual blocks of 64 KB.
    - 32-bit fetch is supported
  - Up to 16 MB of CPU data memory space can map into flash as individual blocks of 64 KB. 8-bit, 16-bit and 32-bit reads are supported

- External memory accessed via a 32 KB read-only cache:
  - Four-way set associative
  - 32-byte cache block
  - Critical word first and early restart

For details, see [ESP32-C6 Technical Reference Manual > Chapter System and Memory](#).

---

### **4.1.2.3 eFuse Controller**

The eFuse memory is a one-time programmable memory that stores parameters and user data, and the eFuse controller of ESP32-C6 is used to program and read this eFuse memory.

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32-C6 Series Datasheet v1.4