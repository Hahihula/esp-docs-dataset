**Title: Chapter 3 GDMA Controller (GDMA)**

---

### Register 3.39. GDMA_IN_PERI_SEL_CHn_REG (n: 0-4) (0x0048+192*n)

| Field | Description |
|-------|-------------|
| Bits [6:5] | Reserved |

**Description:**  
GDMA_PERI_IN_SEL_CHn This register is used to select peripheral for RX channel O. 
0: SPI2; 1: SPI3; 2: UHClO; 3: I2S0; 4: I2S1; 5: LCD_CAM; 6: AES; 7: SHA; 8: ADC_DAC; 9: RMT; 10 ~ 63: Invalid. (R/W)

---

### Register 3.40. GDMA_OUT_PERI_SEL_CHn_REG (n: 0-4) (0x00A8+192*n)

| Field | Description |
|-------|-------------|
| Bits [6:5] | Reserved |

**Description:**  
GDMA_PERI_OUT_SEL_CHn This register is used to select peripheral for TX channel O. 
0: SPI2; 1: SPI3; 2: UHClO; 3: I2S0; 4: I2S1; 5: LCD_CAM; 6: AES; 7: SHA; 8: ADC_DAC; 9: RMT; 10 ~ 63: Invalid. (R/W)

---

### Register 3.41. GDMA_EXTMEM_REJECT_ADDR_REG (0x03F4)

| Field | Description |
|-------|-------------|
| Bits [6] | Reserved |

**Description:**  
GDMA_EXTMEM_REJECTADDR This register stores the first address rejected by permission control when accessing external RAM. (RO) 

---

*Espressif Systems*
*Submit Documentation Feedback*

ESP32-S3 TRM (Version 1.7)