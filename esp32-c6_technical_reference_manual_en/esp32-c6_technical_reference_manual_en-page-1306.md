

```markdown
Chapter 37 Remote Control Peripheral (RMT)

GoBack

37.3.2 RMT RAM

37.3.2.1 Structure of RAM

Figure 37.3-2 shows the format of pulse code in RAM. Each pulse code contains a 16-bit entry with two fields: "level" and "period". "level" (0 or 1) indicates a low-/high-level value that was received or is going to be sent, while "period" points out the number of clock cycles (see clk_div in Figure 37.3-1) that the level lasts for.

[31] [30:16] [15] [14:0]
addr | level | period | level | period

[31] [30:16] * [15] [14:0]
addr | level | period | level | period

Figure 37.3-2. Format of Pulse Code in RAM

The minimum value for the period is zero (0) and is interpreted as a transmission end-marker. For a non-zero period (i.e., not an end-marker), its value is limited by APB clock and RMT clock according to the equation below:

    3 × Tapb_clk + 5 × Tmt_sclk < period × Tclk_div   (1)

37.3.2.2 Use of RAM

The RAM is divided into four 48 x 32-bit blocks. By default, each channel uses one block (block 0 for channel 0, block 1 for channel 1, and so on).

If the data size of one single transfer is larger than the block size of TX channel n or RX channel m, users can configure the channel:

* to enable wrap mode by setting RMT_MEM_TX/RX_WRAP_EN_CHn/m;
* or to use more blocks by configuring RMT_MEM_SIZE_CHn/m.

Setting RMT_MEM_SIZE_CHn/m > 1 allows channel n/m to use the memory of the subsequent channels, i.e., block (n/m) ~ block (n/m + RMT_MEM_SIZE_CHn/m - 1). In such case, the subsequent channels n/m + 1 ~ n/m + RMT_MEM_SIZE_CHn/m - 1 can not be used since their RAM blocks are occupied. For example, if channel 0 is configured to use block 0 and block 1, then channel 1 will be unavailable since its block is occupied, while channel 2 and channel 3 are not affected and can be used normally.

Note that the RAM used by each channel is mapped from low address to high address. In such mode, channel 0 is able to use the RAM blocks of channels 1, 2, and 3 by setting RMT_MEM_SIZE_CHO, but channel 3 can not use the blocks of channels 0, 1, or 2. Therefore, the maximum value of RMT_MEM_SIZE_CHn should not exceed (4 - n) and the maximum value of RMT_MEM_SIZE_CHm should not exceed (2 - m).

The RMT RAM can be accessed via APB bus, or read by the transmitter and written by the receiver. To avoid any possible access conflict between the receiver writing RAM and the APB bus reading RAM, RMT can be
```