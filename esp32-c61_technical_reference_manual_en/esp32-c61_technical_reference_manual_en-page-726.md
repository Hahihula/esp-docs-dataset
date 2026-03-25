

```markdown
- In halfword monitoring mode, `MEM_MONITOR_LOG_CHECK_DATA_REG[15:0]` specifies the monitored halfword.
- In byte monitoring mode, `MEM_MONITOR_LOG_CHECK_DATA_REG[7:0]` specifies the monitored byte.

* Use `MEM_MONITOR_LOG_DATA_MASK_REG` to mask the byte specified in `MEM_MONITOR_LOG_CHECK_DATA_REG`. A masked byte can be any value. For example, if `MEM_MONITOR_LOG_CHECK_DATA_REG` is set to `0x01020304` and `MEM_MONITOR_LOG_DATA_MASK_REG` is set to `0x1`, then any writes matching the `0x010203XX` pattern will be recorded.

4. Configure the storage space for recorded data:

* `MEM_MONITOR_LOG_MEM_START_REG` and `MEM_MONITOR_LOG_MEM_END_REG` specify the storage space for recorded data, which must be in the range of `0x4080_0000` to `0x4084_FFFF`.

* Set `MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG` to update the value in `MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG` to `MEM_MONITOR_LOG_MEM_START_REG`.

* Configure the Debug Assistant module’s permission to access the HP SRAM. The Debug Assistant module can access the HP SRAM only when access permission is enabled. For more information, refer to Chapter 16 Permission Control (PMS).

5. Configure the writing mode for recorded data in loop mode or non-loop mode:

* In loop mode, writing to the specified address space occurs in loops. When writing reaches the end address, it returns to the starting address and continues, overwriting previously recorded data. Set `MEM_MONITOR_LOG_MEM_LOOP_ENABLE` to enable loop mode.

* In non-loop mode, when writing reaches the end address, it stops and discards the remaining data without overwriting previously recorded data. Clear `MEM_MONITOR_LOG_MEM_LOOP_ENABLE` to enable non-loop mode.

  * See examples in Section 18.5.3.1 > step 5.

6. Set `MEM_MONITOR_LOG_DMA_O_ENA` to enable DMA_O channel groups bus access logging.

The Debug Assistant module first writes the DMA recorded data to the internal buffer B, then fetches the data from the buffer and writes it to the configured memory space. When monitored behaviors are triggered continuously, the generated recording packets may fill the buffer, preventing it from accepting new packets. In such cases, the module discards incoming packets and buffers a DMA LOST packet to prevent the buffer from reaching full capacity. The DMA LOST packet contains information about the bus type of the discarded packets, but not the number of discarded packets.

When bus access logging is finished, read the recorded data from memory for decoding. The recorded data is in two packet formats: DMA_O packet (corresponding to DMA_O Data bus) and DMA LOST packet. The packet formats are shown in Table 18.5-5 and 18.5-6.

Table 18.5-5. DMA_O Packet Format

| Bit[31:7] | Bit[6:2] | Bit[1] | Bit[0] |
|-----------|----------|--------|--------|
| addr_offset | dma_source | format | anchored(0) |

Espressif Systems
```