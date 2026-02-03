**Chapter Title:**
Chapter 5 eFuse Controller

**GoBack Link:** GoBack

---

**Section Heading:**
Register 5.101. EFUSE_RD_RS_ERRO_REG (0x10C0)

**Continuation Note:**
Continued from the previous page...

**Subsection with Table and Descriptions for Register 5.102:**

- **EFUSE_KEY3_ERR_NUM:** Represents the number of error bytes during programming KEY3.
  - (RO)
  
- **EFUSE_KEY3_FAIL:** Represents whether or not the data is reliable:
  - O: Means no failure and that the data of key3 is reliable. 
  - 1: Means that programming key3 failed and the number of error bytes is over 6.

- **EFUSE_KEY4_ERR_NUM:** Represents the number of error bytes during programming KEY4.
  - (RO)
  
- **EFUSE_KEY4_FAIL:** Represents whether or not the data is reliable:
  - O: Means no failure and that the data of KEY4 is reliable. 
  - 1: Means that programming data of KEY4 failed and the number of error bytes is over 6.

**Register Description for Register 5.102 (EFUSE_RD_RS_ERR1_REG):**

- **EFUSE_KEY5_ERR_NUM:** Represents the number of error bytes during programming KEY5.
  - (RO)
  
- **EFUSE_KEY5_FAIL:** Represents whether or not the data is reliable:
  - O: Means no failure and that the data of KEY5 is reliable. 
  - 1: Means that programming data of KEY5 failed and the number of error bytes is over 6.

- **EFUSE_SYS_PART2_ERR_NUM:** Represents the number of error bytes during programming system part2.
  - (RO)
  
- **EFUSE_SYS_PART2_FAIL:** Represents whether or not the data is reliable:
  - O: Means no failure and that the data of system part2 is reliable. 
  - 1: Means that programming data of system part2 failed and the number of error bytes is over 6.

**Footer Information:**
Espressif Systems
465 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback