**Title:**
Chapter 15 Permission Control (PMS)

**Register Information:**
- **Register Name:** PMS_DMA_APBPERI_UHCIO_PMS CONSTRAINT_O_REG (0x0048)
- **Field Description:** 
  - **Name:** PMS_DMA_APBPERI_UHCIO_PMS CONSTRAINT_LOCK
  - **Function:** Set this bit to lock UHCIO’s GDMA permission configuration register. (R/W)

**Bit Layout:**
```
+-------------+
|   31       |    0 |
| Reserved   |    0 |
|            +----+----|
|            | 1 | 0 |
|            +----+----|
|            | 0 | 0 |
|            +----+----|
|            | 0 | 0 |
|            +----+----|
|            | 0 | 0 |
|            +----+----|
|            | 0 | 0 |
|            +----+----|
|            | 0 | 0 |
|            +----+----|
|            | 0 | 0 |
|            +----+----|
|            | 0 | 0 |
|            +----+----|
|            | 0 | 0 |
|            +----+----|
```

**Additional Information:**
- **Document Footer:** ESP32-S3 TRM (Version 1.7)
- **Side Texts:**
  - "Espressif Systems"
  - "Submit Documentation Feedback"