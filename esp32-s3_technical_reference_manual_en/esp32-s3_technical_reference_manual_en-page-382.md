**Title: Chapter 3 GDMA Controller (GDMA)**

**Subtitle: Register 3.11. GDMA_IN_INT_RAW_CHn_REG**

**Register Description:** 
- `r: 0-4` `(0x0008+192*n)`

**Bitfield Table:**
```
| 31 | (reserved) |
|----|-------------|
| ... | O           |
|     | O           |
|     | O           |
|     | O           |
|     | O           |
|     | O           |
|     | O           |
|     | O           |
|     | Reset       |
```

**Descriptions:**

- **GDMA_IN_DONE_CHn_INT_RAW:** The raw interrupt bit turns to high level when the last data pointed by one receive descriptor has been received for RX channel 0. (R/WTC/SS)
  
- **GDMA_IN_SUC_EOF_CHn_INT_RAW:** The raw interrupt bit turns to high level for RX channel 0 when the last data pointed by one receive descriptor has been received and the suc_eof bit in this descriptor is 1. For UHCIO, the raw interrupt bit turns to high level when the last data pointed by one receive descriptor has been received and no data error is detected for RX channel 0. (R/WTC/SS)
  
- **GDMA_IN_ERR_EOF_CHn_INT_RAW:** The raw interrupt bit turns to high level when data error is detected only in the case that the peripheral is UHCIO for RX channel 0. For other peripherals, this raw interrupt is reserved. (R/WTC/SS)
  
- **GDMA_IN_DSCR_ERR_CHn_INT_RAW:** The raw interrupt bit turns to high level when detecting receive descriptor error, including owner error, the second and third word error of receive descriptor for RX channel 0. (R/WTC/SS)
  
- **GDMA_IN_DSCR_EMPTY_CHn_INT_RAW:** The raw interrupt bit turns to high level when RX FIFO pointed by inlink is full and receiving data is not completed, but there is no more inlink for RX channel 0. (R/WTC/SS)
  
- **GDMA_INFIFO_FULL_WM_CHn_INT_RAW:** The raw interrupt bit turns to high level when received data byte number is up to threshold configured by GDMA_DMA_INFIFO_FULL_THRS_CHO in RX FIFO of RX channel 0. (R/WTC/SS)

**Footer:**
- "Espressif Systems"
- Page Number: `382`
- Document Version: `ESP32-S3 TRM (Version 1.7)`
- Link Texts:
  - Submit Documentation Feedback
  - GoBack