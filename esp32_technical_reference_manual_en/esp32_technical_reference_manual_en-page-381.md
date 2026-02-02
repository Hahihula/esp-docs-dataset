**Title: Chapter 20 SPI Controller (SPI)**

---

### Register 20.27. SPI_DMA_IN_LINK_REG (0x108)

| Bit | Description |
|-----|-------------|
| 31-29 | Reserved |
| 28   | SPI_INLINK_RESTART Set the bit to add new inlink descriptors. (R/W) |
| 27   | SPI_INLINK_START Set the bit to start to use inlink descriptor. (R/W) |
| 26   | SPI_INLINK_STOP Set the bit to stop to use inlink descriptor. (R/W) |
| 25-0  | Reserved |

**Register Address:** 0x108

---

### Register 20.27. SPI_DMA_IN_LINK_REG (0x108)

| Bit | Description |
|-----|-------------|
| 31   | Reserved |
| 30   | Reserved |
| ...  | ...         |
| 0    | Reset       |

**Register Address:** 0x108

---

### Register 20.28. SPI_DMA_STATUS_REG (0x10C)

| Bit | Description |
|-----|-------------|
| 31   | Reserved |
| 30-29 | Reserved |
| ...  | ...         |
| 0    | Reset       |

**Register Address:** 0x10C

---

### Register 20.28. SPI_DMA_STATUS_REG (0x10C)

| Bit | Description |
|-----|-------------|
| 31   | Reserved |
| 30-29 | Reserved |
| ...  | ...         |
| 0    | Reset       |

**Register Address:** 0x10C

---

#### SPI_DMA_TX_EN
SPI DMA write-data status bit. (RO)

#### SPI_DMA_RX_EN
SPI DMA read-data status bit. (RO)

---

**Footer:**
- Page number: "381"
- Company name and document version information:
  - Espressif Systems ESP32 TRM (Version 5.6)
- Link for submitting documentation feedback.

---