**Title: Chapter 15 Permission Control (PMS)**

---

### Register Information:

- **Register Name:** PMS_EDMA_PMS_SHA_REG  
  **Address:** Ox02F4  

#### Description:
- **Field Details for Register 15.87:**
  - **Name:** PMS_EDMA_PMS_SHA ATTR2
    - **Bits:** 3 to 0 (from right)
      - **Values and Labels:**
        - `3`: Reserved
        - `4`: PMS_EDMA_PMS_SHA ATTR2

- **Functionality Description for Register 15.87:**
  - Configures SHA's access to external SRAM Area0.
    - For details, see Table 15.5-4 (R/W)

- **Field Details for Register 15.88:**
  - **Name:** PMS_EDMA_PMS_ADC_DAC_LOCK_REG
    - **Address:** Ox02F8

#### Description:
- **Functionality Description for Register 15.88:**
  - Set this bit to lock the register that configures ADC Controller's access to external SRAM.
    - For details, see Table 15.5-4 (R/W)

---

### Diagrams and Tables:

**Diagram of Register Layout:**

- **Register Name:** PMS_EDMA_PMS_SHA_REG
  - Address Ox02F4

| Bit | Description |
|-----|-------------|
| 31  | Reserved    |
| ... | ...         |
| 0   | Reset       |

**Description for Register 15.87:**
- **Field Details:** PMS_EDMA_PMS_SHA ATTR2 (Bits from right, starting with `4` to `0`)

**Diagram of Register Layout:**

- **Register Name:** PMS_EDMA_PMS_ADC_DAC_LOCK_REG
  - Address Ox02F8

| Bit | Description |
|-----|-------------|
| 31  | Reserved    |
| ... | ...         |
| 0   | Reset       |

**Description for Register 15.88:**
- **Field Details:** PMS_EDMA_PMS_ADC_DAC_LOCK (Set this bit to lock the register that configures ADC Controller's access to external SRAM)

---

### Additional Information:

- The document is from "ESP32-S3 TRM (Version 1.7)".
- There are references for more details in Table 15.5-4, which specifies read/write permissions and other attributes related to the registers.

---