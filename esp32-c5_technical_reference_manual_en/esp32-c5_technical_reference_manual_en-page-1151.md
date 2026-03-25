

```markdown
Chapter 33 SPI Controller (SPI)

Every input and output data is passing through the Timing Module and the module can be used to apply delay in units of T_clk_spi_mst (one cycle of clk_spi_mst) on rising or falling edge.

Key Registers

*   `SPI_DIN_MODE_REG`: select the latch edge of input data
*   `SPI_DIN_NUM_REG`: select the delay cycles of input data
*   `SPI_DOUT_MODE_REG`: select the latch edge of output data

Timing Compensation Example

Figure 33.8-2 shows a timing compensation example when GP-SPI2 works as master. Note that DUMMY cycle length is configurable to compensate the delay in I/O lines, so as to enhance the performance of GP-SPI2.

![Figure 33.8-2. Timing Compensation Example in GP-SPI2](image)

Configuration

SPI_DIN0_MODE[1:0] = 1, SPI_DIN1_MODE[1:0] = 1,
SPI_DIN0_NUM[1:0] = 0, SPI_DIN1_NUM[1:0] = 1

f_clk_spi_mst/f_SPI_CLK:
    1 -> Adds 1 in dummy cycle length;
others-> Adds 0 in dummy cycle length

Note:
tCLK is delay time of output clock path ("CLK") and the time of clock low to output valid of flash;
tIO is the delay time of FSPID through IO MUX or GPIO matrix;
td is the delay time of FSPIQ relative to FSPID.

In Figure 33.8-2, "p1" is the point of input data of Timing Module, "p2" is the point of output data of Timing Module. Since the input data FSPIQ is unaligned to FSPID, the read data of GP-SPI2 will be wrong without the timing compensation.

To get the correct read data, follow the settings below. Assuming f_clk_spi_mst equals to f_SPI_CLK:

*   Delay FSPID for two cycles at the falling edge of clk_spi_mst.
*   Delay FSPIQ for one cycle at the falling edge of clk_spi_mst.
*   Add one extra dummy cycle.

Espressif Systems
1151
ESP32-C5 TRM (Version 1.0)
Submit Documentation Feedback
```