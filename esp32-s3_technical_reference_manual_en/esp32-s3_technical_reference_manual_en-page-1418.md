**Chapter Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Body Text:**

is configured to use block 0 and block 1, then channel 1 can not be used due to its block being occupied. But channel 2 and channel 3 are not affected, and can be used normally.

Note that the RAM used by each channel is mapped from low address to high address. Under such mapping, channel 0 is able to use the RAM blocks for channels 1, 2 ... and 7 by setting RMT_MEM_SIZE_CHO, but channel 7 cannot use the blocks for channels 0, 1, ..., or 6. Therefore, the maximum value of

RMT_MEM_SIZE_CHm should not exceed (8 - n) and the maximum of 

**Code Block:**
```
RMT_MEM_SIZE_CHm
```

should not exceed (8 - m).

The RMT RAM can be accessed via the APB bus, read by a transmitting channel, and written to by a receiving channel. To avoid any possible access conflict between the receiver writing RAM and the APB bus reading RAM, RMT can be configured to designate the block’s owner, be it the receiver or APB bus, by configuring 

**Code Block:**
```
RMT_MEM_OWNER_CHm
```

If this ownership is violated, a flag signal

**Code Block:**
```
RMT_MEM_OWNER_ERR_CHm
```

will be generated.

When the RMT module is inactive, the RAM can be put into low-power mode by setting 

**Code Block:**
```
RMT_MEMFORCE_PD
```

**Subsection Title (37.3.2.3):**

RAM Access

APB bus is able to access RAM in FIFO mode and in NONFIFO (Direct Address) mode, depending on the configuration of RMT_APB_FIFO_MASK:

- 1: use NONFIFO mode;
- 0: use FIFO mode.

Channels 3 and 7 also support DMA access.

**Subsection Title:** 

FIFO Mode

In FIFO mode, the APB reads data from or writes data to RAM via a fixed address stored in RMT_CHm/mDATA_REG.

**Subsection Title:** 

NONFIFO Mode

In NONFIFO mode, the APB writes data to or reads data from a continuous address range.
- The write-starting address of TX channel n is: RMT base address + 0x800 + (n - 1) x 48. The access address for the second data and the following data are RMT base address + 0x800 + (n - 1) x 48 + 0x4, and so on, incremented by 0x4.
- The read-starting address of RX channel m is: RMT base address + 0x8c0 + (m - 1) x 48. The access address for the second data and the following data are RMT base address + 0x8c0 + (m - 1) x 48 + 0x4, and so on, incremented by 0x4.

**Subsection Title:** 

DMA Mode

Channel 3 also supports DMA access. If 
**Code Block:**
```
RMT_DMA_ACCESS_EN_CH3
```

is set, RAM of channel 3 only allows DMA access. FIFO access or NONFIFO access to channel 3 by the APB bus are forbidden, otherwise unpredictable consequences may occur.

To ensure correct data transmission,

1. DMA should be started first.
2. The write-starting address for TX channels is: RMT base address + (n - 1) x 48; and so on,
3. The read-starting address of RX channel m is:

**Footer Information:** 
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Page Number:**
1418