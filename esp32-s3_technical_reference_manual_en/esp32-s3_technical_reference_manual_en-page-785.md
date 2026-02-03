**Title: Chapter 15 Permission Control (PMS)**

---

### Register Information:

- **Register Name:** PMS_EDMA_PMS_AES_REG (0x2EC)
  - **Description:** Configure AES's access to external SRAM Area0. For details, see Table 15.5-4.
  - **Access Type:** Read/Write
  - **Address Bits:** 31

---

### Register Information:

- **Register Name:** PMS_EDMA_PMS_AES ATTR1 (R/W)
  - **Description:** Configure AES's access to external SRAM Area0.

---

### Register Information:

- **Register Name:** PMS_EDMA_PMS_AES ATTR2
  - **Description:** Configure AES's access to external SRAM Area1. For details, see Table 15.5-4.
  - **Access Type:** Read/Write

---

### Register Information:

- **Register Name:** PMS_EDMA_PMS_SHA_LOCK_REG (0x2F0)
  - **Description:** Set this bit to lock the register that configures SHA's access to external SRAM.

---

**Diagram Description:**

The diagram shows a binary representation of registers with specific bits labeled for different purposes. The labels include "reserved" and numbered positions from top to bottom (e.g., 31, 4-0). There are also indications like "Reset".

**Legend/Key:** 
- PMS_EDMA_PMS_AES ATTR2
- PMS_EDMA_PMS_AES ATTR1

---

**Footer:**
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback