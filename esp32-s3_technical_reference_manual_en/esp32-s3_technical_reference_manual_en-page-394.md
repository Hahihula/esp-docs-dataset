**Title: Chapter 3 GDMA Controller (GDMA)**

---

### Register Section:

- **Register Name:** GDMA_OUT_STATE_CHn_REG  
  - **Address Range:** n = 0-4, Offset: 0x0084+192*n  

#### Binary Representation:
```
| 31 | 23 | 22 | 20 | 19 | 18 | 17 |
|----|----|----|----|----|----|----|
|     |     |     |     |     |     |     |
| 0   | O  | C  | H  | O  | D  | M A_ |
```
- **Description:** This register stores the lower 18 bits of the next receive descriptor address that is pre-read (but not processed yet). If the current receive descriptor is the last descriptor, then this field represents the address of the current receive descriptor.  
  - **Access Type:** Read Only

---

### Register Section:

- **Register Name:** GDMA_OUT_DSCR_STATE_CHn  
  - **Description:** Reserved.

---

### Register Section:

- **Register Name:** GDMA_OUT_STATE_CHn  
  - **Description:** Reserved.
  - **Access Type:** Read Only

---

### Register Section:

- **Register Name:** GDMA_OUT_EOF_DES_ADDR_CHn_REG  
  - **Address Range:** n = 0-4, Offset: 0x0088+192*n  

#### Binary Representation:
```
| 31 | 0x000000 |
|----|----------|
|     |          |
| 0   | O        |
```

- **Description:** This register stores the address of the transmit descriptor when the EOF bit in this descriptor is 1.  
  - **Access Type:** Read Only

---

**Footer:**
- Page Number: 394
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems
- Link Texts:
  - Submit Documentation Feedback