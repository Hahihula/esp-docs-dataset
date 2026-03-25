

```markdown
- or to use more blocks by configuring RMT_MEM_SIZE_CHn/m.

Setting RMT_MEM_SIZE_CHn/m > 1 allows channel n/m to use the memory of the subsequent channels, i.e., block (n/m) ~ block (n/m+RMT_MEM_SIZE_CHn/m−1). In such case, the subsequent channels n/m+1 ~ n/m + RMT_MEM_SIZE_CHn/m−1 can not be used since their RAM blocks are occupied. For example, if channel 0 is configured to use block 0 and block 1, then channel 1 will be unavailable since its block is occupied, while channel 2 and channel 3 are not affected and can be used normally.

Note that the RAM used by each channel is mapped from low address to high address. In such mode, channel 0 is able to use the RAM blocks of channels 1, 2, and 3 by setting RMT_MEM_SIZE_CHO, but channel 3 can not use the blocks of channels 0, 1, or 2. Therefore, the maximum value of RMT_MEM_SIZE_CHn should not exceed (4−n) and the value of RMT_MEM_SIZE_CHm should not exceed (2−m).

The RMT RAM can be accessed via APB bus, or read by the transmitter and written by the receiver. To avoid any possible access conflict between the receiver writing RAM and the APB bus reading RAM, RMT can be configured to designate the RAM block’s owner, be it the receiver or the APB bus, by configuring RMT_MEM_OWNER_CHm. If this ownership is violated, a flag signal RMT_MEM_OWNER_ERR_CHm will be generated.

### 42.3.2.3 RAM Access

APB bus is able to access RAM in FIFO mode and in NONFIFO (Direct Address) mode, depending on the configuration of RMT_APB_FIFO_MASK:

- 0: use FIFO mode;
- 1: use NONFIFO mode.

#### FIFO Mode

In FIFO mode, the APB reads data from or writes data to RAM via a fixed address stored in RMT_CHn/mDATA_REG.

#### NONFIFO Mode

In NONFIFO mode, the APB writes data to or reads data from a continuous address range.

- The write-starting address of TX channel n is (RMT base address + 0x400 + nx48). The access address for the second data and the following data are (RMT base address + 0x400 + nx48 + 0x4), and so on, incremented by 0x4.
- The read-starting address of RX channel m is (RMT base address + 0x460 + mx48). The access address for the second data and the following data are (RMT base address + 0x460 + mx48 + 0x4), and so on, incremented by 0x4.

### 42.3.3 Clock

The clock source of RMT can be PLL_F8OM_CLK, RC_FAST_CLK, or XTAL_CLK, depending on the configuration of PCR_RMT_SCLK_SEL. RMT clock can be enabled by setting PCR_RMT_SCLK_EN. RMT working clock (see rmt_sclk in Figure 42.3-1) is obtained by dividing the selected clock source with a fractional divider. The divider is `PCR_RMT_SCLK_DIV_NUM + 1` / `PCR_RMT_SCLK_DIV_A` / `PCR_RMT_SCLK_DIV_B`
```