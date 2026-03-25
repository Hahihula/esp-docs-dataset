

```markdown
- In loop mode, writing to the specified address space is performed in loops. When writing reaches the end address, it returns to the starting address and continues, overwriting the previously recorded data. Set `MEM_MONITOR_LOG_MEM_LOOP_ENABLE` to 1 to enable loop mode.
For example, there are 10 write operations (1 ~ 10) to address space 0 ~ 4 during bus access. After the 5th operation writes to address 4, the 6th operation will start writing from address 0. The 6th to 10th operations will overwrite the previous data written by the 1st to 5th operations.

- In non-loop mode, when writing reaches the end address, it stops at the end address and dumps the remaining data. The previously recorded data will not be overwritten. Clear `MEM_MONITOR_LOG_MEM_LOOP_ENABLE` to enable non-loop mode.
For example, there are 10 write operations (1 ~ 10) to address space 0 ~ 4 during bus access. After the 5th operation writes to address 4, the 6th to 10th write operations will stop at address 4 and will not be performed any more. Therefore, the address 0 ~ 4 stores the values written by the 1st to 5th operations and the values of the 6th to 10th operations are dumped.

## 6. Configure bus enable registers

- Enable HP CPU, LP CPU, and DMA bus access logging respectively with `MEM_MONITOR_LOG_CORE_ENA`, `MEM_MONITOR_LOG_DMA_1_ENA`, and `MEM_MONITOR_LOG_DMA_O_ENA`. They can be enabled at the same time.
```

**Table 20.5-1. HP CPU Packet Format**

| Bit[63:33] | Bit[32]       | Bit[31:3]     | Bit[2:1]   | Bit[0]    |
|------------|---------------|---------------|----------|-----------|
| pc_offset  | anchored(1)   | addr_offset   | format   | anchored(0)|

**Table 20.5-2. LP CPU Packet Format**

| Bit[31:8] | Bit[7:3] reserved | Bit[2:1] format | Bit[0] anchored(0) |
|-----------|-------------------|----------------|--------------------|
| addr_offset |               |              |                    |

**Table 20.5-3. DMA Packet Format**

| Bit[31:8] | Bit[7:3] dma_source | Bit[2:1] format | Bit[0] anchored(0) |
|-----------|---------------------|----------------|--------------------|
| addr_offset |                 |              |                    |
```