

```markdown
| Value | Source                                                                 |
|-------|------------------------------------------------------------------------|
| 2     | Reserved                                                               |
| 3     | Reserved                                                               |
| 4     | Reserved                                                               |
| 5     | MEM_MONITOR                                                            |
| 6     | TRACE                                                                  |
| 7     | Reserved                                                               |
| 8     | PSRAM_MEM_MONITOR                                                     |
| 9 ~ 15| Reserved                                                               |
| 16 ~ 31| Refer to the peripheral corresponding to the value 0                 |
|       | ~ 15 in Chapter 5 GDMA Controller (GDMA) > Table 5.4-1. For example, a value of 16 matches the peripheral corresponding to 0 in this table, a value of 17 matches the peripheral corresponding to 1 |
```

The internal buffer of the module is 32-bit wide. If HP CPU, LP CPU, and DMA bus access loggings are enabled at the same time, and the record data is generated at the same time, the HP CPU packets are cached into the buffer first, then the DMA packets, and finally the LP CPU packets. The Debug Assistant module will automatically fetch the buffered data and store it in 32-bit data width into the specified memory space.

In loop mode, data looping several times in the storage memory may cause residual data, which can interfere with packet parsing. For example, the lower 32 bits of an HP CPU packet are overwritten, thus making its higher 32 bits residual data. Therefore, users need to filter out the possible residual data when determining the starting position of the first valid packet. Read `MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG` to identify the starting position of the packet, then check the anchored bit value of the packet. If it is 0, retain the data. If it is 1, discard it.

The process of packet parsing is described below.

- Read `MEM_MONITOR_LOG_MEM_FULL_FLAG` to determine whether there is a data overflow.
    - If no, the address space to read is `MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG – 4`.
    - If yes and the loop mode is enabled, the address space is
      `MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG ~ MEM_MONITOR_LOG_MEM_END_REG` and
      `MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG – 4`.
    - If yes and loop mode is not enabled, the address space is `MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_END_REG`.
- Read and parse data from the starting address. Read 32 bits at a time.

After packet parsing is completed, clear the `MEM_MONITOR_LOG_MEM_FULL_FLAG` flag bit by setting `MEM_MONITOR_CLR_LOG_MEM_FULL_FLAG` to 1.

### 20.5.3.2 Bus Access Logging 2 Configuration

Bus access logging 2 includes DMA Bus access logging (external RAM monitoring). The configuration process is described below.
```