**Title: Functional Description**

---

### **4.1.2 Memory Organization**

This subsection describes the memory arrangement to explain how data is stored, accessed, and managed for efficient operation.

Figure 4-1 illustrates the address mapping structure of ESP32-H2:

![Address Mapping Structure](image)

#### Figure Caption:
**Figure 4-1: Address Mapping Structure**

---

### **4.1.2.1 Internal Memory**

The internal memory of ESP32-H2 refers to the memory integrated on the chip die or in the chip package, including ROM, SRAM, eFuse, and flash.

#### Feature List
- 128 KB of ROM for booting and core functions
- 320 KB of high-performance SRAM (HP SRAM) for data and instructions
- 4 KB of low-power SRAM (LP SRAM) that can be accessed by CPU. It can retain data in Deep-sleep mode.
- 4096-bit eFuse memory, with 1792 bits available for users. See also Section **4.1.2.3 eFuse Controller**
- In-package flash
  - Flash size

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-H2 Series Datasheet v1.2