**Title: Chapter 30 SPI Controller (SPI)**

**GoBack**

---

**Register 30.21. SPI_DMA_INT_ST_REG (0x0040)**
Continued from the previous page...

- **SPI_MST_TX_AFIFO_REMPTY_ERR_INT** The status bit for `SPI_MST_TX_AFIFO_REMPTY_ERR_INT` interrupt.
- **SPI_APP2_INT_ST** The status bit for `SPI_APP2_INT` interrupt. (RO)
- **SPI_APP1_INT_ST** The status bit for `SPI_APP1_INT` interrupt.

---

**Register 30.22. SPI_DMA_INT_SET_REG (0x044)**

| Bit | Description |
|-----|-------------|
| 7   | Reserved |
| ... | ... |
| 6   | **SPI_DMA_INFIPO_FULL_ERR_INT** The software set bit for `SPI_DMA_INFIPO_FULL_ERR_INT` interrupt. (WT) |
| 5   | **SPI_DMA_OUTFIFO_EMPTY_ERR_INT** The software set bit for `SPI_DMA_OUTFIFO_EMPTY_ERR_INT` interrupt. (WT) |
| ... | ... |
| 0   | Reserved |

---

**Software Set Bits:**

- **SPI_DMA_INFIPO_FULL_ERR_INT** - The software set bit for `SPI_DMA_INFIPO_FULL_ERR_INT` interrupt.
- **SPI_DMA_OUTFIFO_EMPTY_ERR_INT** - The software set bit for `SPI_DMA_OUTFIFO_EMPTY_ERR_INT` interrupt.

---

**Software Interrupts:**

- **SPI_SLV_EX_QPI_INT_SET**
  - Description: The software set bit for `SPI_SLV_EX_QPI_INT` interrupt.
- **SPI_SLV_EN_QPI_INT_SET**
  - Description: The software set bit for `SPI_SLV_EN_QPI_INT` interrupt.

---

**Software Commands Interrupts:**

- **SPI_SLV_CMD7_INT_SET**
  - Description: The software set bit for `SPI_SLV_CMD7_INT` interrupt.
- **SPI_SLV_CMD8_INT_SET**
  - Description: The software set bit for `SPI_SLV_CMD8_INT` interrupt.

---

**Continued on the next page...**

---

Espressif Systems  
1179  
ESP32-S3 TRM (Version 1.7)  

Submit Documentation Feedback