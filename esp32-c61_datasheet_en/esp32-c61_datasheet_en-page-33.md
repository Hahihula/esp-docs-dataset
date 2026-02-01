Title: Functional Description

---

**4 Figure-1 Address Mapping Structure**

The diagram shows a block structure related to memory mapping in an ESP32-C61 chip.

### Diagram Labels:
- **CPU**
  - CPU Sub-system (0x0000_0000, 0x1FFF_FFFF)
  - ROM (256 KB) (0x4000_0000 to 0x4003_FFFF), HP Memory (320 KB) (0x4080_0000 and 0x4084_FFFF)

- **MMU**
  - Cache (32 KB) (0x41FF_FFFF)
  - GDMA

- **Peripheral**:
  - External Memory
    - Not available for use: 0x600B_FFFF, 0x600C_FFFF, 0x600D_FFFF to 0xFFFF_FFFF
  
### Figure Caption and Description:

**Figure 4-1. Address Mapping Structure**

The internal memory of ESP32-C61 refers to the memory integrated on the chip die or in the chip package, including ROM, SRAM, eFuse, flash, and PSRAM.

---

Subtitle: Internal Memory

Body Text:
The text describes features related to the internal memory:

- **Feature List**
  - 256 KB of ROM for booting and core functions
  - 320 KB of SRAM for data and instructions
  - 4096-bit eFuse memory, with 1792 bits available for users

- In-package flash:
  - See flash size in Chapter 1 ESP32-C61 Series Comparison
  
- More than 100,000 program/erase cycles

---

Footer:

Espressif Systems
Page number: 33
Document title: ESP32-C61 Series Datasheet v0.5