**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Section Header:**
Register 20.25. SPI_DMA_CONF_REG (0x100)

**Binary Register Diagram Description:**
- The diagram shows a binary register with bits labeled from '31' to '0'.
- Each bit is associated with specific functions related to the SPI DMA configuration.

**Bit Descriptions and Functions:**

1. **SPI_DMA_CONTINUE**: This bit enables SPI DMA continuous data TX/RX mode.
   - (R/W)

2. **SPI_DMA_TX_STOP**, **SPI_DMA_RX_STOP**: When in continuous TX/RX mode, setting this bit stops sending/receiving data respectively.

3. **SPI_OUT_DATA_BURST_EN**: SPI DMA reads data from memory in burst mode.
   - (R/W)

4. **SPI_INDESCR_BURST_EN**: SPI DMA reads inlink descriptor in burst mode.
   - (R/W)

5. **SPI_OUTDSCR_BURST_EN**: SPI DMA reads outlink descriptor in burst mode.

6. **SPI_OUT_EOF_MODE**: DMA out-EOF-flag generation mode:
   - 1: out-EOF-flag is generated when DMA has popped all data from the FIFO.
   - 0: out-EOF-flag is generated when DMA has pushed all data to the FIFO.

7. **SPI_AHBM_RST**, **SPI_AHBM_FIFO_RST**: These bits are used for resetting SPI DMA AHB master and FIFO pointer respectively:
   - (R/W)

8. **SPI_OUT_RST**: The bit is used to reset DMA out-FSM and in-data FIFO pointer.
   - (R/W)

9. **SPI_IN_RST**: This bit resets DMA in-DSM.

**Section Header:**
Register 20.26. SPI_DMA_OUT_LINK_REG (0x104)

**Binary Register Diagram Description for this register is similar to the previous one, with bits labeled from '31' to '0'.**

**Bit Descriptions and Functions:**

1. **SPI_OUTLINK_RESTART**: Set the bit to add new outlink descriptors.
   - (R/W)

2. **SPI_OUTLINK_START**, **SPI_OUTLINK_STOP**, **SPI_OUTLINK_ADDR**: These bits are related to starting, stopping, or setting the address of an outlink descriptor respectively:
   - SPI_OUTLINK_START: Set the bit to start using outlink descriptor.
   - SPI_OUTLINK_STOP: Set the bit to stop use outlink descriptor. (R/W)
   - SPI_OUTLINK_ADDR: The address of the first outlink descriptor.

**Footer Information:**
- Page number 380
- Document version ESP32 TRM (Version 5.6)

**Company and Submission Note:**
Espressif Systems  
Submit Documentation Feedback