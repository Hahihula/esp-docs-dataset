**Title: Chapter 15 Permission Control (PMS)**

---

### Register Information:

#### **Register 15.81:** PMS_EDMA_PMS_I2S1_REG (0x02DC)
- Description:
  - **Field Labels**: 
    - `31` to `0`: Reserved
    - `4`, `3`, `2`, `1`, `0`: Reset

- **Functionality**:
  - PMS_EDMA_PMS_I2S1 ATTR1: Configure I2S1's access to external SRAM Area0. For details, see Table 15.5-4.
    - Access Mode (R/W)
  - PMS_EDMA_PMS_I2S1 ATTR2: Configure I2S1's access to external SRAM Area0. For details, see Table 15.5-4.
    - Access Mode (R/W)

---

#### **Register 15.82:** PMS_EDMA_PMS_LCD_CAM_LOCK_REG (0x02E0)
- Description:
  - Set this bit to lock the register that configures Camera-LCD Controller’s access to external SRAM.

- **Functionality**:
  - Access Mode: Read/Write

---

### Diagrams and Tables:

1. **Register 15.81 Diagram** (Binary representation of bits):
   ```
   31 O O O O O O O O O O O O O O
   4 | 3 | 2 | 1 | 0 |
   ```

2. **Register 15.82 Diagram**:
   ```
   31 O O O O O O O O O O O O 
   4 | 3 | 2 | 1 | 0 |
   ```

### Additional Information:

- The document is from "ESP32-S3 TRM (Version 1.7)".
- There are navigation options like "Submit Documentation Feedback" and a back button labeled "Go Back".