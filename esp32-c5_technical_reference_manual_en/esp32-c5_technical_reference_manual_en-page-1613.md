

```markdown
Chapter 42 Remote Control Peripheral (RMT)

The four channels share a 192 x 32-bit RAM.

In the "Clock" frame, the clock-related registers that need to be configured for RMT are specified below:

*   CLK_EN: PCR_RMT_SCLK_EN to enable the rmt_sclk clock
*   CLK_SRC_SEL: PCR_RMT_SCLK_SEL to select the rmt_sclk clock
*   CLK_DIV_NUM: PCR_RMT_SCLK_DIV_NUM to configure the integral part of the divisor for the rmt_sclk clock
*   CLK_DIV_NUMERATOR: PCR_RMT_SCLK_DIV_A to configure the denominator of the divisor's fractional part for the rmt_sclk clock
*   CLK_DIV_DENOMINATOR: PCR_RMT_SCLK_DIV_B to configure the numerator of the divisor's fractional part for the rmt_sclk clock

42.3.2 RAM

42.3.2.1 Structure of RAM

Figure 42.3-2 shows the format of pulse code in RAM. Each pulse code contains a 16-bit entry with two fields: "level" and "period". "level" (0 or 1) indicates a low-/high-level value that has been received or is going to be sent, while "period" points out the number of clock cycles (see clk_div in Figure 42.3-1) that the level lasts for.

![Figure 42.3-2. Format of Pulse Code in RAM](image)

The minimum value for the period is zero (0) and is interpreted as a transmission end-marker. For a non-zero period (i.e., not an end-marker), its value is limited by APB clock and RMT clock according to the formula below:

3 × T_apb_clk + 5 × T_rmt_sclk < period × T_clk_div   (1)

42.3.2.2 Use of RAM

The RAM is divided into four 48 x 32-bit blocks. By default, each channel uses one block (block 0 for channel 0, block 1 for channel 1, and so on).

If the data size of one single transfer is larger than the block size of TX channel n or RX channel m, users can configure the channel:

*   to enable wrap mode by setting RMT_MEM_TX/RX_WRAP_EN_CHn/m;
```