**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Tables and Descriptions**

---

**Table 30.5-14. Supported CMD Values in SPI Mode**

| Transfer Type | CMD[7:0] | CMD State | ADDR State | DATA State |
|---------------|----------|-----------|------------|------------|
| **CMD7**      | 0x24     | 1-bit mode | -         | 4-bit mode |
|               | 0x54     | 1-bit mode | 2-bit mode | 2-bit mode |
|               | 0xA4     | 1-bit mode | 4-bit mode | 4-bit mode |
|               | 0x7      | 1-bit mode | -         | -         |
| **CMD8**      | 0x27     | 1-bit mode | -         | -         |
|               | 0x57     | 1-bit mode | 2-bit mode | -         |
|               | 0xA7     | 1-bit mode | 4-bit mode | -         |
| **CMD9**      | 0x8      | 1-bit mode | -         | -         |
|               | 0x18     | 1-bit mode | -         | -         |
| **CMDA**      | 0x28     | 1-bit mode | -         | -         |
| **CMDDA**     | 0xA8     | 1-bit mode | 4-bit mode | -         |
|               | 0x9      | 1-bit mode | -         | -         |
| **CMDA**      | 0x29     | 1-bit mode | -         | -         |
| **CMDA**      | 0xA9     | 1-bit mode | 4-bit mode | -         |
|               | 0x5A     | 1-bit mode | 2-bit mode | -         |
| **CMDA**      | 0xAA     | 1-bit mode | 4-bit mode | -         |
| End_SEG_TRAN | 0x06     | 1-bit mode | -         | -         |

---

**Table 30.5-15. Supported CMD Values in QPI Mode**

| Transfer Type | CMD[7:0] | CMD State | ADDR State | DATA State |
|---------------|----------|-----------|------------|------------|
| Wr_BUFS       | 0xA1     | 4-bit mode | -         | 4-bit mode |
| Rd_BUFS       | 0xA2     | 4-bit mode | -         | 4-bit mode |
| Wr_DMA        | 0xA3     | 4-bit mode | -         | 4-bit mode |
| Rd_DMA        | 0xA4     | 4-bit mode | -         | 4-bit mode |
| CMD7          | 0x27     | 1-bit mode | -         | -         |
| CMD8          | 0xA8     | 4-bit mode | -         | -         |
| CMD9          | 0xA9     | 4-bit mode | -         | -         |
| CMDA          | 0xAA     | 1-bit mode | -         | -         |
| End_SEGTrans | 0xA5     | 4-bit mode | -         | -         |
| Ex_QPI        | 0xDD     | 4-bit mode | -         | -         |

---

**Text Description:**

Master sends 0x06 CMD (En_QPI) to set GP-SPI slave to QPI mode and all the states of supported transfer will be in 4-bit mode afterwards. If 0xDD CMD (Ex_QPI) is received, GP-SPI slave will be back to SPI mode.

**Footer:**
Espressif Systems
1138 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback