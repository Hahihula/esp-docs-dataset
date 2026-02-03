**Title: Chapter 3 GDMA Controller (GDMA)**

**Subtitle: Register 3.30. GDMA_OUTFIFO_STATUS_CHn_REG (n: 0-4) (0x0078+192\*n)**

**Table Description:**  
The table lists various registers related to the GDMA OUT FIFO status for different channels and their respective functions.

| Bit Position | Register Name                          |
|--------------|----------------------------------------|
| 31           | Reserved                               |
| 27-0         | GDMA_OUT_REMAIN_UNDER_4B_L3_CHn        |
|              | (reserved)                             |
| 26           | GDMA_OUT_REMAIN_UNDER_3B_L3_CHn        |
| 25           | GDMA_OUT_REMAIN_UNDER_1B_L3_CHn        |
| 24           | GDMA_OUT_REMAIN_UNDER_0B_L3_CHn        |
| 23           | GDMA_OUT_REMAIN_UNDER_4B_L2_CHn        |
| 22           | GDMA_OUT_REMAIN_UNDER_3B_L2_CHn        |
| 21           | GDMA_OUT_REMAIN_UNDER_1B_L2_CHn        |
| 20           | GDMA_OUT_REMAIN_UNDER_0B_L2_CHn        |
| 19           | GDMA_OUTFIFO_FULL_L4_CHn               |
|              | L4 TX FIFO full signal for TX channel n (RO) |
| 18           | GDMA_OUTFIFO_EMPTY_L4_CHn              |
|              | L4 TX FIFO empty signal for TX channel n (RO) |
| 17-0         | GDMA_OUTFIFO_FULL_L3_CHn               |
|              | L3 TX FIFO full signal for TX channel o. (RO) |
| 16           | GDMA_OUTFIFO_EMPTY_L3_CHn              |
|              | L3 TX FIFO empty signal for TX channel n (RO) |
| 15-0         | GDMA_OUTFIFO_CNT_L4_CHn                |
|              | The register stores the byte number of data in L4 TX FIFO for TX channel o. (RO) |
| 14           | GDMA_OUTFIFO_FULL_L2_CHn               |
| 13           | GDMA_OUTFIFO_EMPTY_L2_CHn              |
| 12-0         | GDMA_OUTFIFO_FULL_L1_CHn               |
| 11           | GDMA_OUTFIFO_EMPTY_L1_CHn              |
| 10           | GDMA_OUTFIFO_CNT_L3_CHn                |
| 9            | GDMA_OUT_REMAIN_UNDER_4B_L2_CHn        |
| 8            | GDMA_OUT_REMAIN_UNDER_3B_L2_CHn        |
| 7            | GDMA_OUT_REMAIN_UNDER_1B_L2_CHn        |
| 6            | GDMA_OUT_REMAIN_UNDER_0B_L2_CHn        |
| 5-0          | GDMA_OUT_REMAIN_UNDER_4B_L1_CHn        |
|              | L1 TX FIFO full signal for TX channel o. (RO) |
| 4            | GDMA_OUT_REMAIN_UNDER_3B_L1_CHn        |
| 3            | GDMA_OUT_REMAIN_UNDER_1B_L1_CHn        |
| 2            | GDMA_OUT_REMAIN_UNDER_0B_L1_CHn        |
| 1            | GDMA_OUTFIFO_FULL_L0_CHn               |
|              | L0 TX FIFO full signal for TX channel o. (RO) |
| 0            | GDMA_OUTFIFO_EMPTY_L0_CHn              |
|              | L0 TX FIFO empty signal for TX channel n (RO) |

**Descriptions:**
- **GDMA_OUTFIFO_FULL_L1_CHn:** L1 TX FIFO full signal for TX channel o. (RO)
- **GDMA_OUTFIFO_EMPTY_L1_CHn:** L1 TX FIFO empty signal for TX channel l.0. (RO)
- **GDMA_OUTFIFO_FULL_L2_CHn:** L2 TX FIFO full signal for TX channel 0. (RO)
- **GDMA_OUTFIFO_EMPTY_L2_CHn:** L2 TX FIFO empty signal for TX channel o. (RO)
- **GDMA_OUTFIFO_FULL_L3_CHn:** L3 TX FIFO full signal for TX channel l.0. (RO)
- **GDMA_OUTFIFO_EMPTY_L3_CHn:** L3 TX FIFO empty signal for TX channel n. (RO)
- **GDMA_OUTFIFO_CNT_L1_CHn:** The register stores the byte number of data in L1 TX FIFO for TX channel o. (RO).
- **GDMA_OUTFIFO_CNT_L2_CHn:** The register stores the byte number of data in L2 TX FIFO for TX channel 0. (RO)
- **GDMA_OUTFIFO_CNT_L3_CHn:** The register stores the byte number of data in L3 TX FIFO for TX channel o. (RO)

**Reserved Registers:**
- GDMA_OUT_REMAIN_UNDER_1B_L3_CHn
- GDMA_OUT_REMAIN_UNDER_2B_L3_CHn
- GDMA_OUT_REMAIN_UNDER_3B_L3_CHn

**Other Reserved Register:**  
GDMA_OUT_REMAIN_UNDER_4B_L3_CHn (RO)

**Footer:**
Espressif Systems  
Page 393 ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)