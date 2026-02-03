**Title: Chapter 15 Permission Control (PMS)**

---

### Register Information:

- **Register Name:** PMS_CORE_O_VECBASE OVERRIDE_2_REG (0x01C4)
  - **Description:** Configures the VECBASE value for the Non-secure World. (R/W)

#### Binary Representation:
```
+-------------+---------------------------+
| 31 | 22 | 21 | ... | 0 |
+-------------+---------------------------+
| 0   | 0   | 0   | ... | 0 |
+-------------+---------------------------+
```

- **Field Description:** 
  - `PMS_CORE_O_VECBASE OVERRIDE_WOLD1_VALUE` (bit positions: reserved, 31 to 22)
  
---

### Register Information:

- **Register Name:** PMS_EDMA_BOUNDARY_LOCK_REG (0x02A8)
  - **Description:** Set this bit to lock EDMA boundary registers. (R/W)

#### Binary Representation:
```
+-------------+---------------------------+
| 31 | ... |... | ... | 0 |
+-------------+---------------------------+
| 0   | 0   | 0   | ... | 0 |
+-------------+---------------------------+
```

- **Field Description:** 
  - `PMS_EDMABOUNDARY_LOCK` (bit positions: reserved, 31 to some other bit)

---

**Footer Information:**
- "Submit Documentation Feedback" on the left side.
- Page number and document version information at the bottom center.