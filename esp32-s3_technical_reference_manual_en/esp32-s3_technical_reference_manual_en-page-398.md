**Title: Chapter 3 GDMA Controller (GDMA)**

---

### Register 3.42. GDMA_EXTMEM_REJECT_ST_REG (0x03F8)

| Field Name | Offset |
|------------|--------|
| Reserved   |        |

- **GDMA_EXTMEM_REJECT_PERI_NUM**  
  - Description: Read or write attribute of the rejected access.
  - Details:
    - Bit O: if this bit is 1, the rejected access is WRITE. (RO)
    - Bit I: if this bit is 1, the rejected access is READ.

- **GDMA_EXTMEM_REJECT_CHANNEL_NUM**  
  - Description: This field indicates the channel used for the rejected access.
  - Access Type: Read Only

- **GDMA_EXTMEM_REJECT_PERI_NUM**  
  - Description: This bit indicates the peripheral whose access was rejected.
  - Access Type: Read Only

---

### Register 3.43. GDMA_DATE_REG (0x040C)

| Field Name | Offset |
|------------|--------|
| Reserved   |        |

- **GDMA_DATE**  
  - Description: This is the version control register.

---

*Espressif Systems*

*Submit Documentation Feedback*

ESP32-S3 TRM (Version 1.7)