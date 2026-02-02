**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.1 DMABUSMODE_REG (0x0000)

**Continuation Note:**
Continued from the previous page...

**Body Text with Descriptions and Registers:**

- **PROG_BURST_LEN**: These bits indicate the maximum number of beats to be transferred in one DMA transaction. If the number of beats to be transferred is more than 32, then perform the following steps:
  - Set the PBLx8 mode
  - Set the PBL

**Register Description:**
- **ALT_DESC_SIZE**: When set, the size of the alternate descriptor increases to 32 bytes. (R/W)
- **DESC SKIP LEN**: This bit specifies the number of Word to skip between two unchained descriptors.
  The address skipping starts from the end of current descriptor to the start of next descriptor.

**Additional Information:**
When the DSL(DESC SKIP LEN) value is equal to zero, the descriptor table is taken as contiguous by the DMA in Ring mode. (R/W)

- **DMA_ARB_SCH**: This bit specifies the arbitration scheme between the transmit and receive paths.
  - 'b0: weighted round-robin with RX: TX or TX: RX
  - 'b1 Fixed priority (Rx priority to Tx). (R/W)
  
- **SW_RST**: When this bit is set, the MAC DMA Controller resets the logic all internal registers of the MAC. It is cleared automatically after the reset operation complete in all of the ETH_MAC clock domains.

**Additional Information:**
Before reprogramming any register of the ETH_MAC you should read a zero (0) value in this bit.
(R/W/SC)

**Register Address and Description for Section 24.2 DMATXPOLLDemand_REG (0x0004):**

- **TRANS POLL DEMAND**: When these bits are written with any value, the DMA reads the current descriptor to which the Register (Current Host Transmit Descriptor Register) is pointing.
  - If that descriptor is not available (owned by the Host), the transmission returns to the suspend state and Bit[2] of Status Register is asserted. 
  - If the descriptor is available, the transmission resumes.

**Register Address and Description for Section 24.3 DMARXPOLLDemand_REG (0x0008):**

- **RECV POLL DEMAND**: When these bits are written with any value, the DMA reads the current descriptor to which the Current Host Receive Descriptor Register is pointing.
  - If that descriptor is not available (owned by the Host), the reception returns to the Suspended state and Bit[7] of Status Register is asserted. 
  - If the descriptor is available, the Rx DMA returns to the active state.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number:** ESP32 TRM (Version 5.6) Page 489