**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Figure Caption and Diagram Description:**
- **Figure:** Figure 30.8-2, Timing Compensation Example in GP-SPI2 Master Mode

**Diagram Labels:**
- clk_hclk
- clk_spi_mst
- FSPID
- FSPIQ
- tClk (delay time of output clock path)
- tO (the delay time of FSPID through IO MUX or GPIO matrix)

**Diagram Annotations in Red Text on the Right Side:** 
- p1, before Timing Module
- A B [timing diagram elements]
- p2, after Timing Module

**Diagram Annotations at Bottom:**
- GP-SPI2 read data (A and B with timing markers)
- Note:
  - tClk is delay time of output clock path ('Clk') and the time of clock low to output valid.
  - tO is the delay time of FSPID through IO MUX or GPIO matrix;
    - tClk: cycle length, others: Adds a dummy cycle length
  - tD is the delay time of FSPIQ relative to FSPID.

**Body Text Explanation:** 
- In Figure 30.8-2:
  - "p1" refers to input data point.
  - "p2" points at output data in Timing Module, assuming unaligned SPIQ and FSPIQ leads to wrong read data without timing compensation for GP-SPI2.

**Instructions:**
To get correct read data follow these settings (assuming fClk_spi_mst equals to fSpi_clk):
- Delay FSPID by two cycles on the falling edge of clk_spi_mst.
- Delay FSPIQ one cycle at the falling edge of clk_spi_mst.
- Add an extra dummy cycle.

**Additional Information:**
In GP-SPI2 slave mode, if SPI_RSCK_DATA_OUT in register SPI_SLAVE_REG is set to 1:
- Output data sent on latch edge (half a clock earlier) for timing compensation. 

**Footer Text:** 
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Page Number:**
1147