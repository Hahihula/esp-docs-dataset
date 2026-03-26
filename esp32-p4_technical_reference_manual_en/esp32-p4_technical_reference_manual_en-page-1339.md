

```markdown
Chapter 21 Debug Assistant

CPU1 packet (corresponding to HP CPU1 Data bus), and HP CPU LOST packet. The packet formats are shown in Table 21.5-1 and 21.5-2.

Table 21.5-1. HP CPUO/1 Packet Format

| Bit[63:33] | Bit[32]   | Bit[31:3]    | Bit[2:1] | Bit[0] |
|------------|-----------|--------------|----------|--------|
| pc_offset  | anchored (1) | addr_offset  | format   | anchored (0) |

Table 21.5-2. HP CPU LOST Packet Format

| Bit[31:7] | Bit[6:3]    | Bit[2:1] | Bit[0] |
|-----------|-------------|----------|--------|
| reserved  | lost_source | format   | anchored (0) |

It can be seen from the data packet formats that the size of the HP CPUO/1 packet is 64 bits and that of the HP CPU LOST packet is 32 bits. These packets contain the following fields:

* `format` – the packet type. O: HP CPUO packet; 1: HP CPU1 packet; 2: HP CPU LOST packet; 3: Reserved.
* `pc_offset` – the offset of the HP CPUO/1 PC register at the time of access. Actual PC = pc_offset + 0x0000_0000.
* `addr_offset` – the address offset of a write operation. Actual address = addr_offset + SPM_MEM_MONITOR_LOG_MIN_REG[31:4], '4'h0.
* `lost_source` – the dumped packets when the HP CPU LOST packet was generated.

    - Bit[4:3]: 0 indicates HP CPUO packets were not dumped. 3 indicates HP CPUO packets were dumped. Other values are reserved.
    - Bit[6:5]: 0 indicates HP CPU1 packets were not dumped. 3 indicates HP CPU1 packets were dumped. Other values are reserved.

* `anchored` – the location of the 32 bits in the data packet. 0: Lower 32 bits. 1: Higher 32 bits.

The internal buffer of the module is 32 bits wide. When the HP CPUO and HP CPU1 bus access loggings are both enabled and the record data is generated at the same time, the HP CPUO data packets are first buffered, then the HP CPU1 packets. The Debug Assistant will automatically fetch the buffered data and store it in 32-bit data width into the specified memory space.

In loop mode, data looping several times in the storage memory may cause residual data, which can interfere with packet parsing. For example, the lower 32 bits of a HP CPUO/1 packet are overwritten, thus making its higher 32 bits residual data. Therefore, users need to filter out the possible residual data in order to determine the starting position of the first valid packet with `SPM_MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG`. Once the starting position of the packet is identified, check the anchored bit value of the packet. If it is 0, the data will be retained. If it is 1, it will be dumped.

The process of packet parsing is described below:

* Determine whether there is a data overflow with `SPM_MEM_MONITOR_LOG_MEM_FULL_FLAG`.

    - If no, the address space to read is `SPM_MEM_MONITOR_LOG_MEM_START_REG ~ SPM_MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG - 4`.
```