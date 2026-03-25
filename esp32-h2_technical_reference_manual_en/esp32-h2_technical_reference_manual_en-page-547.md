

```markdown
It can be seen from the data packet formats that the HP CPU packet size is 64 bits, DMA packet size 32 bits, and LOST packet 32 bits. These packets contain the following fields:

*   **format** – the packet type. 0: CPU packet; 1: DMA packet; 3: LOST packet.
*   **pc_offset** – the offset of the PC register at the time of access. Actual PC = pc_offset + 0x4000_0000.
*   **addr_offset** – the address offset of a write operation. Actual address = addr_offset + MEM_MONITOR_LOG_MIN_REG.
*   **dma_source** – the source of DMA access. For more information, please refer to Chapter 15 Permission Control (PMS) > Table 15.4-1.
*   **anchored** – the location of the 32 bits in the data packet. 1 indicates the lower 32 bits. 2 indicates the higher 32 bits.

The internal buffer of the module is 32 bits wide. When the CPU or DMA bus access logging are all enabled at the same time and the record data is generated at the same time, the DMA data packets are first buffered, and then the CPU packets. The Debug Assistant will automatically fetch the buffered data and store it in 32-bit data width into the specified memory space.

In Loop mode, data looping several times in the configured storage address space may cause residual data, which can interfere with packet parsing. For example, the lower 32 bits of a CPU packet are overwritten, thus making its higher 32 bits residual data. Therefore, users need to filter out the possible residual data in order to determine the starting position of the first valid packet with MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG. Once the starting position of the packet is identified, check the anchored bit value of the packet. If it is 1, the data will be retained. If it is 2, it will be discarded.

The process of packet parsing is described below:

1.  Determine whether there is a data overflow with MEM_MONITOR_LOG_MEM_FULL_FLAG:
    *   If no, the address space to read is MEM_MONITOR_LOG_MEM_START_REG – MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG - 4.
    *   If yes and Loop mode is enabled, the address space is MEM_MONITOR_
        LOG_MEM_CURRENT_ADDR_REG – MEM_MONITOR_LOG_MEM_END_REG and
        MEM_MONITOR_LOG_MEM_START_REG – MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG - 4.
    *   If yes and Loop mode is not enabled, the address space is
        MEM_MONITOR_LOG_MEM_START_REG – MEM_MONITOR_LOG_MEM_END_REG.

2.  Read and parse data from the starting address. Read 32 bits each time.

After packet parsing is completed, clear the MEM_MONITOR_LOG_MEM_FULL_FLAG flag bit by setting MEM_MONITOR_CLR_LOG_MEM_FULL_FLAG.
```

```markdown
## 17.5 Register Summary

The addresses of bus logging configuration registers (see 17.5.1) in this section are relative to the MEM_MONITOR base address. The addresses of other registers (see 17.5.2) are relative to the ASSIST_DEBUG
```