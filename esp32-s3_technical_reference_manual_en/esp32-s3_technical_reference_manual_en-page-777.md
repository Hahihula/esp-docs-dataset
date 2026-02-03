**Title: Chapter 15 Permission Control (PMS)**

---

### Register Information:

- **Register Name:** PMS_EDMA_BOUNDARY_0_REG  
  **Address:** `0x02AC`  
  **Description:** Configures the ending address of external SRAM area0. For details, see Table 15.5-3.
  - **Access Type:** (R/W)  

**Bit Description:**
- Bit 31 to bit 14 is reserved.

---

### Register Information:

- **Register Name:** PMS_EDMA_BOUNDARY_1_REG  
  **Address:** `0x02B0`  
  **Description:** Configures the ending address of external SRAM area1. For details, see Table 15.5-3.
  - **Access Type:** (R/W)  

**Bit Description:**
- Bit 31 to bit 14 is reserved.

---

### Diagrams:

There are two diagrams showing a register layout with bits labeled from `0` at the leftmost position, increasing towards right up to `31`. The diagram indicates that certain positions of these registers (specifically around address locations) have specific values or functions. For example:
- In PMS_EDMABOUNDARY_0, bit 0 is set as "Reset".
- Similarly in PMS_EDMABOUNDARY_1, the value at position `31` to some bits are shown with a hexadecimal representation like `0x2000`.

---

**Footer:**
- **Document Version:** ESP32-S3 TRM (Version 1.7)
- **Navigation Links:** Submit Documentation Feedback | GoBack