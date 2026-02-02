**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**GoBack Link:** [GoBack](#)

---

**Section Header - Register Description and Values**

- **Register Name**: DMATXCURRDESC_REG (0x0048)
  - **Field**: 
    - **Name**: TRANS_DSCR_ADDR_PTR
    - **Description**: The address of the current receive descriptor list. Cleared on Reset.
    - **Access Mode**: Pointer updated by the DMA during operation. (RO)

- **Register Name**: DMARXCURRDESC_REG (0x004C)
  - **Field**:
    - **Name**: RECV_DSCR_ADDR_PTR
    - **Description**: The address of the current receive descriptor list. Cleared on Reset.
    - **Access Mode**: Pointer updated by the DMA during operation. (RO)

- **Register Name**: DMATXCURRADDR_BUF_REG (0x0050)
  - **Field**:
    - **Name**: TRANS_BUFF_ADDR_PTR
    - **Description**: The address of the current receive descriptor list. Cleared on Reset.
    - **Access Mode**: Pointer updated by the DMA during operation. (RO)

- **Register Name**: DMARXCURRADDR_BUF_REG (0x0054)
  - **Field**:
    - **Name**: RECV_BUFF_ADDR_PTR
    - **Description**: The address of the current receive descriptor list. Cleared on Reset.
    - **Access Mode**: Pointer updated by the DMA during operation. (RO)

---

**Footer:**
- Page Number: 499
- Company Name: Espressif Systems
- Document Title: ESP32 TRM (Version 5.6)
- Link Texts:
  - Submit Documentation Feedback

(Note: The image contains a table with hexadecimal values and reset indicators, but the specific details are not transcribed here as per instructions.)