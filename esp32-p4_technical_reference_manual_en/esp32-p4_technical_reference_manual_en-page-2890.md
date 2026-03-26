
```markdown
Chapter 57 Remote Control Peripheral (RMT)

GoBack

57.3.2.2 Use of RAM

The RAM is divided into eight 48 × 32-bit blocks. By default, each channel uses one block (block 0 for channel 0, block 1 for channel 1, and so on).

If the data size of one single transfer is larger than one block size of TX channel n or RX channel m, users can configure the channel:

- to enable wrap mode by setting RMT_MEM_TX/RX_WRAP_EN_CHn/m;
- or to use more blocks by configuring RMT_MEM_SIZE_CHn/m.

Setting RMT_MEM_SIZE_CHn/m > 1 allows channel n/m to use the memory of the subsequent channels, i.e., block (n/m) ~ block (n/m + RMT_MEM_SIZE_CHn/m - 1). In such case, the subsequent channels (n/m + 1) ~ (n/m + RMT_MEM_SIZE_CHn/m - 1) can not be used since their RAM blocks are occupied. For example, if channel 0 is configured to use block 0 and block 1, then channel 1 will be unavailable since its block is occupied, while channel 2 and channel 3 are not affected and can be used normally.

Note that the RAM used by each channel is mapped from low address to high address. Under such mapping, channel 0 is able to use the RAM blocks for channels 1, 2 ... and 7 by setting RMT_MEM_SIZE_CHO, but channel 7 can not use the blocks for channels 0, 1, ... or 6. Therefore, the value of RMT_MEM_SIZE_CHn should not exceed (8 - n) and the value of RMT_MEM_SIZE_CHm should not exceed (8 - m).

The RMT RAM can be accessed via APB bus, or read by the transmitter and written by the receiver. To avoid any possible access conflict between the receiver writing RAM and the APB bus reading RAM, RMT can be configured to designate the RAM block’s owner, be it the receiver or the APB bus, by configuring RMT_MEM_OWNER_CHm. If this ownership is violated, a flag signal RMT_MEM_OWNER_ERR_CHm will be generated.

57.3.2.3 RAM Access

APB bus is able to access RAM in FIFO mode and in NONFIFO (Direct Address) mode, depending on the configuration of RMT_APB_FIFO_MASK:

- 0: Use FIFO mode;
- 1: Use NONFIFO mode.

Channels 3 and 7 also support GDMA access.

FIFO Mode

In FIFO mode, the APB reads data from or writes data to RAM via a fixed address stored in RMT_CHn/mDATA_REG.

NONFIFO Mode

In NONFIFO mode, the APB writes data to or reads data from a continuous address range.

- The write-starting address of TX channel n is: RMT base address + 0x800 + nx48. The access address for the second data and the following data are RMT base address + 0x800 + nx48 + 0x4, and so on, incremented by 0x4.
- The read-starting address of RX channel m is: RMT base address + 0x8C0 + mx48. The access address for the second data and the following data are RMT base address + 0x8C0 + mx48 + 0x4, and so on, incremented by 0x4.
```