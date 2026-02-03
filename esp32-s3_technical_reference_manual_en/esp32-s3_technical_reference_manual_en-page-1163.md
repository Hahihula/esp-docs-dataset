**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Register Information:**
- Register Name: SPI_SLAVE_REG (0x00E0)
- Bitfield Description:
  - `SPI_USR_CONF` to `SPI_DMA_SEG_MAGIC_VALUE`
  - Each bit has a specific function related to the SPI clock and data handling.

**Bitfield Details in Table Format with Descriptions for Each Field from Left to Right:**
1. **SPI_CLK_MODE**: 
   - Description:
     - 0: SPI clock is off when CS becomes inactive.
     - 1: SPI clock is delayed one cycle after CS becomes inactive.
     - 2: SPI clock is delayed two cycles after CS becomes inactive.
     - 3: SPI clock is always on.

2. **SPI_CLK_MODE_13**:
   - Description:
     - 0: Support SPI clock mode 0 and 2, output data B[1]/B[6] at the first edge of rising edge (R/W).
     - 1: Output data D[0]/D[7] to support SPI clock modes.

3. **SPI_RSCK_DATA_OUT**:
   - Description:
     - Save half a cycle when TSCK is the same as RSCK.
     - 1: Output data at RSCK rising edge (R/W).
     - 0: Output data at TSCK falling edge or always on in some modes.

4. **SPI_SLV_RDDMA_BITLEN** and related fields:
   - Description for `SPI_SLV_RDDMA_BITLEN` to `SPI_SLV_WRDMA_BITLEN` with corresponding bit lengths (R/W) used during Rd_DMA transfer, Wr_DMA transfer.
   - If set: Store data bit length of Rd_BUf transfer or Wr_BUf transfer.

5. **SPI_SLV_WRBUFF_BITLEN**:
   - Description for storing the data bit length when SPI_SLAVE_DATA_BITLEN is not in use (R/W).

6. **SPI_DMA_SEG_MAGIC_VALUE**: 
   - Description: Configure magic value of BM table in DMA-controlled configurable segmented transfer, only applicable to SPI2.

7. **SPI_SLAVE_MODE**:
   - Description for setting SPI work mode.
     - 1: Slave mode
     - 0: Master mode

8. **SPI_SOFT_RESET**:
   - Description: Software reset enable bit (R/W).
   - If set in CONF state, resets the clock line and data lines.

9. **SPI_USR_CONF**: 
   - Description for SPI2 only.
   - Enable or disable the CONF state of current DMA-controlled configurable segmented transfer to start a configurable segment transfer; 1: Start it, 0: Not applicable (R/W).

**Footer Information:**
- Document Title and Version:
  - ESP32-S3 TRM (Version 1.7)
- Company Name:
  - Espressif Systems
- Page Number/Section Reference:
  - Submit Documentation Feedback

This document provides detailed information about the configuration bits for an SPI controller, including their functions in different modes of operation and how they affect data transfer processes within a system using the ESP32-S3 microcontroller.