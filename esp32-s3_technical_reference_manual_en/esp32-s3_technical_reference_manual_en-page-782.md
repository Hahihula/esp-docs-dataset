**Title: Chapter 15 Permission Control (PMS)**

---

### Register Information:

- **Register Name:** PMS_EDMA_PMS_I2SO_REG (0x02D4)
  - **Description:** 
    - `PMS_EDMA_PMS_I2SO ATTR1`: Configures I2S0's access to external SRAM Area. For details, see Table 15.5-4.
    - `PMS_EDMA_PMS_I2SO ATTR2`: Configures I2S0’s access to external SRAM Area. For details, see Table 15.5-4.

- **Register Name:** PMS_EDMA_PMS_I2S1_LOCK_REG (0x02D8)
  - **Description:**
    - `PMS_EDMA_PMS_I2S1 LOCK`: Set this bit to lock the register that configures I2S1's access to external SRAM. For details, see Table 15.5-4.

---

**Diagram Description (Binary Representation):**

- The diagram shows a binary representation of two registers:
  - **Register PMS_EDMA_PMS_I2SO_REG:**
    - Bits are labeled from `31` down to `0`.
    - Specific bits (`PMS_EDMA_PMS_I2SO ATTR1`, `PMS_EDMA_PMS_I2SO ATTR2`) have specific functions as described above.
  - **Register PMS_EDMA_PMS_I2S1_LOCK:**
    - Similar binary representation with the bit labeled from `31` down to `0`.
    - The only significant setting is indicated by a note that says "Set this bit".

---

**Footer Information:**  
- Document version and feedback information are present but not fully visible in the image. 

**Navigation Links:**
- Left side navigation includes options like “Submit Documentation Feedback”.
- Right sidebar has an option to go back.

---