**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**Section Header:**
Register 3.2. GDMA_IN_CONF1_CHn_REG (n: 0-4) (0x0004+192*n)

**Diagram Description:**
A binary register diagram with labels for each bit position from most significant to least, ranging from 'reserved' at the top down through various bits labeled as follows:
- GDMA_IN_EXT_MEM_BK_SIZE_Q
- GDMA_IN_CHECK_OWNER CHO
- GDMA_DMA_INFO_FULL_THRS_CHO

**Text Description:**
GDMA_DMA_INFIFO_FULL_THRS_CHn This register is used to generate the GDMA_INFIFO_FULL_WM_INT interrupt when RX channel 0 received byte number in RX FIFO is up to the value of the register. (R/W)

**Subsection Header and Text:**
GDMA_IN_CHECK_OWNER_CHn Set this bit to enable checking the owner attribute of the descriptor. (R/W)

**Text Description for another Register:**
GDMA_IN_EXT_MEM_BK_SIZE_CHn Block size of RX channel 0 when GDMA access external RAM.
- O: 16 bytes; 1: 32 bytes; 2: 64 bytes; 3: Reserved. (R/W)

**Section Header and Text for another Register:**
Register 3.3. GDMA_IN_POP_CHn_REG (n: 0-4) (0x001C+192*n)

**Diagram Description of Another Binary Register:**
A binary register diagram similar to the first, with labels from most significant bit down through various bits labeled as follows:
- GDMA_INFO_POP_CHO
- GDMA_INFO_RDATA_CHO

**Text Description for another Register:**
GDMA_INFIFO_RDATA_CHn This register stores the data popping from GDMA FIFO (intended for debugging). (RO)

**Text Description of Another Register:**
GDMA_INFIFO_POP_CHn Set this bit to pop data from GDMA FIFO (intended for debugging). (R/W/SC)

**Footer Information:**
Espressif Systems
377 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback