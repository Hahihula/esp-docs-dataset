**Chapter 3: GDMA Controller (GDMA)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **GDMA_IN_PERI_SEL_CH4_REG** | Peripheral selection of RX channel 4 | 0x0348 | R/W |
| **GDMA_OUT_PERI_SEL_CH4_REG** | Peripheral selection of TX channel 4 | 0x03A8 | R/W |

---

### Permission Status Registers

- GDMA_EXTMEM_REJECT_ADDR_REG
  - Description: External RAM address where access violation occurs
  - Address: 0x03F4
  - Access: RO
  
- GDMA_EXTMEM_REJECT_ST_REG
  - Description: Status of external RAM where access violation occurs
  - Address: 0x03F8
  - Access: RO

---

### Version Register

- **GDMA_DATE_REG**
  - Description: Version control register
  - Address: 0x040C
  - Access: R/W

---

**Espressif Systems**

**Submit Documentation Feedback**

ESP32-S3 TRM (Version 1.7)