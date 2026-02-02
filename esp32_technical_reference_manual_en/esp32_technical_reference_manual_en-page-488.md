**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Register Name and Address:**
Register 24.1, DMABUSMODE_REG (0x0000)

**Table Description:**
The table shows the bit layout of Register 24.1 with various fields such as DMAMIXEDBURST, PBLX8_MODE, USE_SEP_PBL, RX_DMA_PBL, FIXED_BURST, and PRI_RATIO.

- **DMAMIXEDBURST:** When this bit is set high and FB(FIXES_BURST) bit is low, the AHB master interface starts all bursts of a length more than 16 with INCR (undefined burst), whereas it reverts to fixed burst transfers (INCRx and SINGLE) for burst length of 16 and less. (R/W)
- **PBLX8_MODE:** When set high, this bit multiplies the programmed PBL(PROG_BURST_LEN) value eight times. Therefore, the DMA transfers the data in sizes: 8, 16, 32, 64, 128, and 256 beats depending on the PBL value. (R/W)
- **USE_SEP_PBL:** When set high, this bit configures the Rx DMA to use the value configured in Bits[22:17] as PBL. The PBL value in Bits[13:8] is applicable only for the Tx DMA operations. When reset to low, the PBL value in Bits[13:8] is applicable for both DMA engines. (R/W)
- **RX_DMA_PBL:** This field indicates the maximum number of beats to be transferred in one Rx DMA transaction. The maximum that can use a single block Read or Write. The Rx DMA always attempts to burst as specified in RPBL(RX_DMA_PBL) bit each time it starts a burst transfer on the host bus.
- **FIXED_BURST:** This bit controls whether the AHB master interface performs fixed burst transfers, not when set; When set, the AHB interface uses only SINGLE, INCR4, INCR8, or INCR16 during start of normal burst transfers. When reset: The AHB interface uses SINGLE and INCR burst transfer operations.
- **PRI_RATIO:** These bits control the priority ratio in weighted round-robin arbitration between Rx DMA and Tx DMA.

**Additional Information on PRI_RATIO:**
The values are represented by each bit:
- 2^b00 — 1 : 1
- 2^b01 — 2 : 0
- 2^b10 — 3 : 1
- 2^b11 — 4 : 1

**Footer:**
Continued on the next page...

**Company and Document Information:**
Espressif Systems  
Page number: 488  
Document version: ESP32 TRM (Version 5.6)  

**Navigation Links at Bottom of Page:** 
- Submit Documentation Feedback