**Title: Functional Description**

---

### **4.1.3 External Flash and RAM**

ESP32 supports multiple external QSPI flash and external RAM (SRAM) chips. More details can be found in ESP32 Technical Reference Manual > Chapter SPI Controller. ESP32 also supports hardware encryption/decryption based on AES to protect developers’ programs and data in flash.

ESP32 can access the external QSPI flash and SRAM through high-speed caches.
- Up to 16 MB of external flash can be mapped into CPU instruction memory space and read-only memory space simultaneously.
  - When external flash is mapped into CPU instruction memory space, up to 11 MB + 248 KB can be mapped at a time. Note that if more than 3 MB + 248 KB are mapped, cache performance will be reduced due to speculative reads by the CPU.
  - When external flash is mapped into read-only data memory space, up to 4 MB can be mapped at a time. 8-bit, 16-bit and 32-bit reads are supported.

- External RAM can be mapped into CPU data memory space. SRAM up to 8 MB is supported and up to 4 MB can be mapped at a time. 8-bit, 16-bit and 32-bit reads and writes are supported.
  
**Note:**
After ESP32 is initialized, firmware can customize the mapping of external RAM or flash into the CPU address space.

---

### **4.1.4 Address Mapping Structure**

The structure of address mapping is shown in Figure 4-1. The memory and peripheral mapping is shown in Table 4-1.
  
**Figure:**
- Title: ESP32 Series Datasheet v5.2
- Page Number: 27

---

### **Table (Not fully visible, only partial content provided):**

| Address Range | Memory/Peripheral |
|---------------|------------------|
| 0x0000_0000  | 0x3F3F_FFFF      |
| 0x004C_2000  |                  |
| ...          | ...              |

---

**Figure Caption:**
- Title: Address Mapping Structure

---

**Footer:** 
Espressif Systems  
Submit Documentation Feedback