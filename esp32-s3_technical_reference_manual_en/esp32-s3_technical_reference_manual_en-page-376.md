**Title:**
Chapter 3 GDMA Controller (GDMA)

**Subtitle:**
3.8 Registers

**Body Text:**
The addresses in this section are relative to GDMA base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Table Description:**
Register 3.1. GDMA_IN_CONF0_CHn_REG (n: 0-4) (0x0000+192*n)

| Bit | Name                          |
|-----|-------------------------------|
| 31  | GDMA_MEMTrans_EN_CH0         |
|     |                               |
| 5   | GDMA_INData_Burst_EN_CH0    |
|     |                               |
| 4   | GDMA_INLoopTest_EN_CH0      |
|     |                               |
| 3   | GDMA_INRST_CH0               |
|     |                               |
| 2   | Reserved                      |
| 1   | GDMA_INLoopTest_CHn         |
|     |                               |
| 0   | Reset                         |

**List Items:**
- GDMA_IN_RST_CHn This bit is used to reset GDMA channel O RX FSM and RX FIFO pointer. (R/W)
- GDMA_IN_LOOP_TEST_CHn Reserved. (R/W)
- GDMA_INDSCR_BURST_EN_CHn Set this bit to 1 to enable INCR burst transfer for RX channel 0 reading descriptor when accessing internal RAM. (R/W)
- GDMA_IN_DATA_BURST_EN_CHn Set this bit to 1 to enable INCR burst transfer for RX channel 0 receiving data when accessing internal RAM. (R/W)
- GDMA_MEMTrans_EN_CHn Set this bit to 1 to enable automatic transmitting data from memory to memory via GDMA. (R/W)

**Footer:**
Espressif Systems
376 ESP32-S3 TRM (Version 1.7)