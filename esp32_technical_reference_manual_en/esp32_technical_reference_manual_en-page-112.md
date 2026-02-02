**Title: Chapter 5 eFuse Controller (EFUSE)**

---

### Register 5.25. EFUSE_INT_ST_REG (0x10c)

| Bit | Description |
|-----|-------------|
| **31-0** | Reserved |

EFUSE_PGM_DONE_INT_ST  
The masked interrupt status bit for the EFUSE_PGM_DONE_INT interrupt. (RO)  

EFUSE_READDone_INT ST  
The masked interrupt status bit for the EFUSE_READ_DONE_INT interrupt. (RO)  

---

### Register 5.26. EFUSE_INT_ENA_REG (0x110)

| Bit | Description |
|-----|-------------|
| **31-0** | Reserved |

EFUSE_PGM_DONE_INT ENA  
The interrupt enable bit for the EFUSE_PGMDone_INT interrupt. (R/W)  

EFUSE_READDONE_INT ENA  
The interrupt enable bit for the EFUSE_READ_DONE_INT interrupt. (R/W)  

---

### Register 5.27. EFUSE_INT_CLR_REG (0x114)

| Bit | Description |
|-----|-------------|
| **31-0** | Reserved |

EFUSE_PGM_DONE_INT CLR  
Set this bit to clear the EFUSE_PGM_DONE_INT interrupt. (WO)  

EFUSE_READDONE_INT CLR  
Set this bit to clear the EFUSE_READ_DONE_INT interrupt. (WO)  

---

*Espressif Systems*  
112  
ESP32 TRM (Version 5.6)

[Submit Documentation Feedback](#)