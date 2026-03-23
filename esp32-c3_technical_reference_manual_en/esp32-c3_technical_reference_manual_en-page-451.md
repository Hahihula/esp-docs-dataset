

```markdown
| Value | Source |
|-------|--------|
| 5     | SHA    |
| 6     | ADC    |
| 7     | I2S    |
| 8     | reserved |
| 9     | reserved |
| 10    | reserved |
| 11    | UHClO  |
| 12    | reserved |
| 13    | reserved |
| 14    | reserved |
| 15    | reserved |

Table 17.4-4. Written Data Format

| Bit[127:3]           | Bit[2:0]     |
|----------------------|--------------|
| Valid packets        | START_FLAG   |

Since the CPU packet size is 50 bits and the DMA packet size 25 bits, the recorded data in each record is at least 25 bits and at most 75 bits. When the data stored in the internal buffer reaches 125 bits, it will be popped into memory. There are cases where a packet is divided into two portions: the first portion is written to memory, and the second portion is left in the buffer and will be popped into memory in the next write. The data left in the buffer is called residual data. The value of START_FLAG records the number of residual bits left from the last write to memory. The number of residual bits is START_FLAG * 25. START_FLAG also indicates the starting bit of the first valid packet in the current write. As an example: Assume that four DMA writes have generated four DMA packets to be stored in the buffer with a total of 100-bit data. Then, one CPU write occurs and generates one 50-bit CPU packet. The buffer will pop the previously-recorded 100-bit data plus the first 25 bits in the CPU packet into SRAM. The remaining 25 bits in the CPU packet is left in the buffer, waiting for the next write. START_FLAG in the next write will indicate that 25 bits in this write is from the last write.

In loop writing mode, if data is looped several times in the storage memory, the residual data will interfere with packet parsing. Therefore, users need to filter out the residual data in order to determine the starting position of the first valid packet with START_FLAG and ASSIST_DEBUG_LOG_MEM_CURRENT_ADDR_REG. Once the starting position of the packet is identified, the subsequent data is continuous and users do not need to care about the value of START_FLAG.

Note that if data in the buffer does not reach 125 bits, it will not be written to memory. All data should be written to memory for packet parsing. This can be done by disabling bus access logging. When ASSIST_DEBUG_LOG_ENA is set to 0, if there is data in the buffer, it will be padded with zeros from the left until it becomes 128 bits long and written to the memory.

The process of packet parsing is described below:

*   Determine whether there is a data overflow with ASSIST_DEBUG_LOG_MEM_FULL_FLAG. If there is no overflow, ASSIST_DEBUG_LOG_MEM_START_REG is the starting address of the first packet. If there is an
```