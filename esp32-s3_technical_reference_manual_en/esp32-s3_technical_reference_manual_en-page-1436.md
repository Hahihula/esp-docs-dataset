**Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Header:**
GoBack

**Register Information:**
- **Name:** RMT_INT_ENA_REG (0x0078)
- **Description:** Interrupt enable register for the remote control peripheral.

**Bit Description Table:**

| Bit Number | Name                          |
|------------|-------------------------------|
| 31         | Reserved                      |
| ...        | ...                           |
| 2          | RMT_CHn_TX_END_INT_ENA (n = 0-3) The interrupt enable bit of RMT_CHn_TX_END_INT. (R/W) |
|           |                               |
| 1          | RMT_CHn_ERR_INT_ENA (n = 0-3) The interrupt enable bit of RMT_CHn_ERR_INT. (R/W) |
| ...        | ...                           |
| 2         | RMT_CHn_TXTHR_EVENT_INT_ENA (n = 0-3) The interrupt enable bit of RMT_CHn_TXTHR_EVENT_INT. (R/W) |
|           |                               |
| 1          | RMT_CHn_TX_LOOP_INT_ENA (n = 0-3) The interrupt enable bit of RMT_CHn_TX_LOOP_INT. (R/W) |
| ...        | ...                           |
| 2         | RMT_CHm_RX_END_INT_ENA (m = 4-7) The interrupt enable bit of RMT_CHm_RX_END_INT. (R/W) |
|           |                               |
| 1          | RMT_CHm_ERR_INT_ENA (m = 4-7) The interrupt enable bit of RMT_CHm_ERR_INT. (R/W) |
| ...        | ...                           |
| 2         | RMT_CHm_RX_THR_EVENT_INT_ENA (m = 4-7) The interrupt enable bit of RMT_CHm_RX_THR_EVENT_INT. (R/W) |
|           |                               |
| 1          | RMT_CH3_DMA_ACCESS_FAIL_INT_ENA The interrupt enable bit of RMT_CH3_DMA_ACCESS_FAIL_INT. (R/W) |
| ...        | ...                           |
| 2         | RMT_CH7_DMA_ACCESS_FAIL_INT_ENA The interrupt enable bit of RMT_CH7_DMA_ACCESS_FAIL_INT. (R/W) |

**Footer:**
Espressif Systems
1436 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback