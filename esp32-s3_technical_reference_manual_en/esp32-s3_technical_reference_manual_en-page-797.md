**Title: Chapter 15 Permission Control (PMCS)**

---

### Register Information:

- **Register Name:** SYSCON_FLASH_ACEn_ADDR_REG  
  - **Description:** Address register for Flash Region n. The address should be aligned to CA_R8.
  - **Address Range:** 0x033 + 4*n
  - **Access Mode:** (R/W)

#### Register Details:
- **Register Number:** 15.103  
- **Bits Description:**
  - `SYSCON_FLASH_ACEn_ADDR_S`: Starting address of Flash Region n.

---

### Register Information:

- **Register Name:** SYSCON_FLASH_ACEo_ADDR_S
  - **Description:** Configure the starting address of Flash Region o.
  - **Size Alignment:** The size should be aligned to 64 KB. (R/W)

#### Register Details:
- **Register Number:** 15.104  
- **Bits Description:**
  - `SYSCON_FLASH_ACEo_SIZE REG`: Size register for Flash Region o.

---

### Register Information:

- **Register Name:** SYSCON_FLASH_ACEn_SIZE
  - **Description:** Configure the length of Flash Region n.
  - **Size Alignment:** The size should be aligned to 64 KB. (R/W)

#### Register Details:
- **Register Number:** Not specified in this section.

---

**Footer:**
- "Submit Documentation Feedback"
- Page number indicated as `797`
- Document version mentioned at the bottom left corner, "(Version 1.2)"