

```markdown
- Configure the permission for the Debug Assistant module to access the internal HP SRAM. Only when the access permission is enabled can the Debug Assistant module access the internal HP SRAM. For more information, please refer to Chapter 16 Permission Control (PMS).
```

5. Configure the writing mode for the recorded data: loop mode or non-loop mode.

- In loop mode, writing to the specified address space is performed in loops. When writing reaches the end address, it will return to the starting address and continue, overwriting the previously recorded data. Set `MEM_MONITOR_LOG_MEM_LOOP_ENABLE` to enable loop mode.
  For example, there are 10 write operations (1 ~ 10) to address space 0 ~ 4 during bus access. After the 5th operation writes to address 4, the 6th operation will start writing from address 0. The 6th to 10th operations will overwrite the previous data written by the 1th to 5th operations.

- In non-loop mode, when writing reaches the end address, it will stop at the end address and dump the remaining data, not overwriting the previously recorded data. Clear `MEM_MONITOR_LOG_MEM_LOOP_ENABLE` to use non-loop mode.
  For example, there are 10 write operations (1 ~ 10) to address space 0 ~ 4 during bus access. After the 5th operation writes to address 4, the 6th to 10th write operations will stop at address 4 and will not be performed any more. Therefore, the address 0 ~ 4 stores the values written by the 1 ~ 5 operations and the values of the 6 ~ 10 operations are dumped.

6. Configure bus enable registers.

- Enable HP CPU, LP CPU, or DMA bus access logging with `MEM_MONITOR_LOG_ENA`. They can be enabled at the same time.

The Debug Assistant module first writes the recorded data to an internal buffer, and then fetches the data from the buffer and writes it to the configured memory space. When the monitored behaviors are triggered continuously, the generated recording packets may fully occupy the buffer, making it unable to take any incoming packets. At this time, the module dumps these incoming packets and buffers a LOST packet instead before the buffer reaches its capacity. However, the bus type and the number of these dumped packets are unknown.

When bus access logging is finished, the recorded data can be read from memory for decoding. The recorded data is in four packet formats, namely HP CPU packet (corresponding to HP CPU Data bus), LP CPU packet (corresponding to LP CPU bus), DMA packet (corresponding to DMA bus), and LOST packet. The packet formats are shown in Table 18.4-1, 18.4-2, 18.4-3, and 18.4-4.

Table 18.4-1. HP CPU Packet Format

| Bit[63:34] | Bit[33:32] | Bit[31:4] | Bit[3:2] | Bit[1:0] |
|------------|------------|-----------|----------|----------|
| pc_offset  | anchored(2)| addr_offset| format   | anchored(1) |

Table 18.4-2. LP CPU Packet Format

| Bit[31:4] | Bit[3:2] | Bit[1:0] |
|-----------|----------|----------|
| addr_offset| format   | anchored(1) |

Table 18.4-3. DMA Packet Format
```