**Title: Chapter 5 eFuse Controller (EFUSE)**

---

### Register 5.14. EFUSE_BLK0_WDATA6_REG (0x034)

| Bit | Description |
|-----|-------------|
| 31-28 | Reserved |
| 27   | EFUSE_KEY_STATUS This field programs the value of key_status. (R/W) |
| 26   | EFUSE_DISABLE_DL_CACHE This field programs the value of download_dis_cache. (R/W) |
| 25   | EFUSE_DISABLE_DL_DECRYPT This field programs the value of download_dis_decrypt. (R/W) |
| 24   | EFUSE_DISABLE_DL_ENCRYPT This field programs the value of download_dis_encrypt. (R/W) |
| 23   | EFUSE_DISABLE_JTAG This field programs the value of JTAG_disable. (R/W) |
| 22   | EFUSE_ABS_DONE_1 This field programs the value of abstract_done_1. (R/W) |
| 21   | EFUSE_ABS_DONE_0 This field programs the value of abstract_done_0. (R/W) |
| 20-3  | EFUSE_CONSOLE_DEBUG_DISABLE This field programs the value of console_debug.disable. (R/W) |
| 29    | Reserved |
| 30    | EFUSE_CODING_SCHEME This field programs the value of coding_scheme. (R/W) |

---

### Register 5.15. EFUSE_BLK1_RDATAₙ Regiment (n: 0-7) (0x38+4*n)

| Bit | Description |
|-----|-------------|
| 31   | Reserved |
| 0    | This field returns the value of word n in BLOCK1. (RO) |

---

### Register 5.16. EFUSE_BLK2_RDATAₙ Regiment (n: 0-7) (0x58+4*n)

| Bit | Description |
|-----|-------------|
| 31   | Reserved |
| 0    | This field returns the value of word n in BLOCK2. (RO) |

---

**Footer:**  
Espressif Systems  
Submit Documentation Feedback

ESP32 TRM (Version 5.6)

--- 

*Note: The image contains a diagram with binary values and labels, but it is not described here as per instructions.*