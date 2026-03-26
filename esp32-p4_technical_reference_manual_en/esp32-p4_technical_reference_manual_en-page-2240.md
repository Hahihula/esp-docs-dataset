

```markdown
Figure 43.8-2. Timing Compensation Example in GP-SPI2 as Master

In Figure 43.8-2, “p1” is the point of input data of Timing Module, “p2” is the point of output data of Timing Module. Since the input data SPI2Q is unaligned to SPI2D, the read data of GP-SPI2 will be wrong without the timing compensation.

To get the correct read data, follow the settings below. Assuming f_clk_spi_mst equals to f_SPI_CLK:

*   Delay SPI2D for two cycles at the falling edge of clk_spi_mst.
*   Delay SPI2Q for one cycle at the falling edge of clk_spi_mst.
*   Add one extra dummy cycle

When GP-SPI works as slave, if the bit SPI_RSCK_DATA_OUT in register SPI_SLAVE_REG is set to 1, the output data is sent at latch edge, which is half an SPI clock cycle earlier. This can be used for slave mode timing compensation.

## 43.9 LP-SPI Wake-Up

LP-SPI supports wake-up feature when working as a slave. When LP-SPI is in a sleep state (set LP_SPI_SLEEP_EN to 1), it can generate a wake_up signal and trigger PMU to wake up the chip by configuring LP_SPI_SLV_WK_MODE_SEL to select the wake up mode. For the detailed wake-up flow, see Chapter 14 Low-Power Management.

*   When LP_SPI_SLV_WK_MODE_SEL = 0, LP-SPI wakes up the chip after detecting the start bit.
*   When LP_SPI_SLV_WK_MODE_SEL = 1, LP-SPI wakes up the chip after receiving a specific character sequence.
```