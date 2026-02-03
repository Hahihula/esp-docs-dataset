**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**GoBack Link:** GoBack

---

**Section Header: Register 3.25. GDMA_IN_SUC_EOF_DES_ADDR_CHn_REG**

- **Description of the register:**
  - `GDMA_IN_SUC_EOF_DES_ADDR_CHn` This register stores the address of the receive descriptor when the EOF bit in this descriptor is 1.
  
**Register Address and Offset Description:** 
- `0x0028+192*n`

---

**Section Header: Register 3.26. GDMA_IN_ERR_EOF_DES_ADDR_CHn_REG**

- **Description of the register:**
  - `GDMA_IN_ERR_EOF_DES_ADDR_CHn` This register stores the address of the receive descriptor when there are some errors in current receiving data.
  
**Register Address and Offset Description:** 
- `0x002C+192*n`

---

**Section Header: Register 3.27. GDMA_IN_DSCR_CHn_REG**

- **Description of the register:**
  - `GDMA_IN_DSCR_CHn` Represents the address of the next receive descriptor x+1 pointed by the current receive descriptor that is pre-read.
  
**Register Address and Offset Description:** 
- `0x030+192*n`

---

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version:**
ESP32-S3 TRM (Version 1.7)