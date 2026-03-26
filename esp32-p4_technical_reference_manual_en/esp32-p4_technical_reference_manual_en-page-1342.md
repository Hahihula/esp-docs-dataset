

```markdown
Chapter 21 Debug Assistant GoBack


Table 21.5-3. DMA_2 Packet Format

| Bit[31:9] | Bit[8:4] | Bit[3:1] | Bit[0] |
|-----------|----------|----------|--------|
| addr_offset0 | reserved | format   | anchored (O) |

Table 21.5-4. DMA_3 Packet Format

| Bit[31:9] | Bit[8:4] | Bit[3:1] | Bit[0] |
|-----------|----------|----------|--------|
| addr_offset1 | reserved | format   | anchored (O) |

Table 21.5-5. DMA LOST Packet Format

| Bit[31:10] | Bit[9:8] | Bit[7:4] | Bit[3:1] | Bit[0] |
|------------|----------|----------|----------|--------|
| reserved   | lost_source | reserved | format   | anchored (O) |

It can be seen from the data packet formats that the size of the DMA_2, DMA_3, and DMA LOST packet is 32 bits. These packets contain the following fields:

* `format` – the packet type. 4: DMA_2 packet; 5: DMA_3 packet; 6: DMA LOST packet; other values: Reserved.
* `addr_offset0` - the address offset of a write operation. Actual address = addr_offset0 + L2_MEM_MONITOR_LOG_MIN_REG[31:5],5'h0.
* `addr_offset1` - the address offset of a write operation. Actual address = addr_offset1 + L2_MEM_MONITOR_LOG_MIN_REG[31:2],2'h0.
* `lost_source` - the dumped packets when the DMA LOST packet was generated.

    - Bit[8]: 0 indicates DMA_2 packets were not dumped. 1 indicates DMA_2 packets were dumped.
    - Bit[9]: 0 indicates DMA_3 packets were not dumped. 1 indicates DMA_3 packets were dumped.
* `anchored` - the location of the 32 bits in the data packet. 0: Lower 32 bits. 1: Higher 32 bits.

The internal buffer of the module is 32 bits wide. When the bus access loggings of DMA_2 and DMA_3 channel groups are both enabled and the record data is generated at the same time, the DMA_2 data packets are first buffered, then the DMA_3 packets. The Debug Assistant will automatically fetch the buffered data and store it in 32-bit data width into the specified memory space.

The process of packet parsing is described below:

* Determine whether there is a data overflow with L2_MEM_MONITOR_LOG_MEM_FULL_FLAG.
    - If no, the address space to read is L2_MEM_MONITOR_LOG_MEM_START_REG ~ L2_MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG - 4.
    - If yes and the loop mode is enabled, the address space is
        L2_MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG ~
        L2_MEM_MONITOR_LOG_MEM_END_REG and L2_MEM_MONITOR_LOG_MEM_START_REG ~
        L2_MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG - 4.
    - If yes and loop mode is not enabled, the address space is
        L2_MEM_MONITOR_LOG_MEM_START_REG ~ L2_MEM_MONITOR_LOG_MEM_END_REG.

Espressif Systems          1342          ESP32-P4 TRM
Submit Documentation Feedback PRELIMINARY
```