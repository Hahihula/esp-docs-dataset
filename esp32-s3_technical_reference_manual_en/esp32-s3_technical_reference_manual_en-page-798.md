**Title: Chapter 15 Permission Control (PIS)**

---

### Register Information:

- **Register Name:** SYSCON_SRAM_ACEn ATTR_REG (0x0058)
- **Description:** Configures the permission to Region n of SRAM. (R/W)

#### Details:
- **Address Offset:** 15.105
- **Bit Positions:**
  - **Bits 9, 8, and 0** are reserved.
  
| Bit | Description |
|-----|-------------|
| 31 to 24 | Reserved bits (0) |
| 23 | Reset bit |

---

### Register Information:

- **Register Name:** SYSCON_SRAM_ACEn ADDR_REG (n: 0-3) (0x0068 + 4*n)
- **Description:** Configures the starting address of SRAM Region n. The size of each region should be aligned to 64 KB. (R/W)

#### Details:
- **Address Offset:** 15.106
- **Bit Positions:**
  - **Bits 31** is a reset bit.
  
| Bit | Description |
|-----|-------------|
| 31 | Reset bit |

---

### Footer Information:

- Document Version: ESP32-S3 TRM (Version 1.7)
- Feedback Link: Submit Documentation Feedback

--- 

*Note: The image also contains diagrams with binary representations and labels, but they are not described in text form as per the instructions.*