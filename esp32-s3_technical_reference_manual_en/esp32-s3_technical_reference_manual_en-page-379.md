**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**Section Header:**
GoBack

**Register Information for Register 3.5 - GDMA_OUT_CONF0_CHn_REG**

- **Register Description:** 
  - `GDMA_OUT_RST_CHn`: This bit is used to reset GDMA channel 0 TX FSM and TX FIFO pointer.
  - `GDMA_OUT_LOOP_TEST_CHn`: Reserved (R/W)
  - `GDMA_OUT_AUTO_WRBAC_CHn`: Set this bit to enable automatic outlink-writeback when all the data in TX FIFO has been transmitted. (R/W)
  - `GDMA_OUT_EOF_MODE_CHn`: EOF flag generation mode when transmitting data.
    - 1: EOF flag for TX channel 0 is generated when data need to transmit has been popped from FIFO in GDMA. (R/W)
  - `GDMA_OUTDSCR_BURST_EN_CHn`: Set this bit to 1 to enable INCR burst transfer for TX channel reading descriptor when accessing internal RAM.
  - `GDMA_OUT_DATA_BURST_EN_CHn`: Set this bit to 1 to enable INCR burst transfer for TX channel transmitting data when accessing internal RAM.

**Register Information for Register 3.6 - GDMA_OUT_CONF1_CHn_REG**

- **Register Description:** 
  - `GDMA_OUT_CHECK_Owner_CHn`: Set this bit to enable checking the owner attribute of the descriptor.
  - `GDMA_OUT_EXT_MEM_BK_SIZE_CHn`: Block size of TX channel 0 when GDMA access external RAM. (R/W)

**Footer:**
Espressif Systems
379 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback