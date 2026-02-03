**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**GoBack Link:** GoBack

---

**Register Section Header and Description for Register 3.7:**

- **Title:** Register 3.7. GDMA_OUT_PUSH_CHn_REG (n: 0-4) (0x07C+192*n)
  
  - **Diagram/Visualization of the register layout with labels such as `GDMA_OUTFIFO_PUSH CHO`, `GDMA_OUTFIFO_WDATA CHO`, etc., and binary positions from bits 31 to bit 8.**
  
- **Description:** GDMA_OUTFIFO_WDATA_CHn: This register stores the data that need to be pushed into GDMA FIFO.
  - **Access Type:** (R/W)
  
- **Description:** GDMA_OUTFIFO_PUSH_CHn
  - Set this bit to push data into GDMA FIFO. (R/W/SC)

---

**Register Section Header and Description for Register 3.8:**

- **Title:** Register 3.8. GDMA_OUT_LINK_CHn_REG (n: 0-4) (0x080+192*n)
  
  - **Diagram/Visualization of the register layout with labels such as `GDMA_OUTLINK PARK CHO`, `GDMA_OUTLINK START CHO`, etc., and binary positions from bits 31 to bit 1.
  
- **Description:** GDMA_OUTLINK_ADDR_CHn
  - This register stores the two least significant bits of the first transmit descriptor’s address. (R/W)
  
- **Description:** GDMA_OUTLINK_STOP_CHn
  - Set this bit to stop GDMA’s transmit channel from transferring data. (R/W/SC)
  
- **Description:** GDMA_OUTLINK_START_CHn
  - Set this bit to enable GDMA’s transmit channel for data transfer. (R/W/SC)
  
- **Description:** GDMA_OUTLINK_RESTART_CHn
  - Set this bit to restart a new outlink from the last address. (R/W/SC)
  
- **Description:** GDMA_OUTLINK_PARK_CHn: 
 1: the transmit descriptor’s FSM is in idle state; O: the transmit descriptor’s FSM is working. (RO)

---

**Footer Information:**
Espressif Systems
380 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback