**Chapter Title:**
Chapter 18 SHA Accelerator (SHA)

**GoBack Link:** GoBack

---

**Section Header and Description with Register Information**

- **Register Name**: SHA_DMA_CONTINUE_REG (0x0020)
  - **Description**: Write 1 to continue DMA-SHA calculation. (WO)
  - **Binary Representation Diagram**: [Binary representation of the register is shown]

- **Register Name**: SHA_INT_CLEAR_REG (0x0024)
  - **Description**: Clears DMA-SHA interrupt. (WO)
  - **Binary Representation Diagram**: [Binary representation of the register is shown]
  - **Field Description**:
    - **SHA_CLEAR_INTERRUPT**: Enables clearing of DMA-SHA interrupt.

- **Register Name**: SHA_INT_ENA_REG (0x0028)
  - **Description**: Enables DMA-SHA interrupt. (R/W)
  - **Binary Representation Diagram**: [Binary representation of the register is shown]
  - **Field Description**:
    - **SHA_INTERRUPT_ENA**: Enables DMA-SHA interrupt.

- **Register Name**: SHA_DATE_REG (0x002C)
  - **Description**: Version control register. (R/W)
  - **Binary Representation Diagram**: [Binary representation of the register is shown]
  - **Field Description**:
    - **SHA_DATE**: Version information, with a specific value "0x20190402" provided.

---

**Footer Information:**
- Company Name: Espressif Systems
- Document Title and Version Info: ESP32-S3 TRM (Version 1.7)
- Page Number: 855

**Action Links:** Submit Documentation Feedback