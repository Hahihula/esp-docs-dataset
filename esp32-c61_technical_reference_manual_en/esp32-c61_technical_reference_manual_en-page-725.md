

```markdown
The module's internal buffer is 32 bits wide. If the HP CPU and DMA bus access logging are enabled simultaneously and data is recorded at the same time, the HP CPU packets are cached in the buffer first, followed by the DMA packets. The Debug Assistant module automatically fetches the buffered data and stores it in the specified memory space with a 32-bit data width.

In loop mode, data looping multiple times in the storage memory may cause residual data, which can interfere with packet parsing. For example, the lower 32 bits of an HP CPU packet may overwrite, leaving higher 32-bit residual data. Therefore, users must filter out possible residual data when determining the starting position of the first valid packet. Read `MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG` to identify the starting position of the packet, then check the anchored bit value of the packet. If it is 0, retain the data. If it is 1, discard it.

The packet parsing process is described below.

*   Read `MEM_MONITOR_LOG_MEM_FULL_FLAG` to determine whether there is a data overflow.
    -   If no, the address space to read is `MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG – 4`.
    -   If yes and loop mode is enabled, the address space is
        `MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG ~ MEM_MONITOR_LOG_MEM_END_REG` and
        `MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG – 4`.
    -   If yes and loop mode is not enabled, the address space is `MEM_MONITOR_LOG_MEM_START_REG ~ MEM_MONITOR_LOG_MEM_END_REG`.

*   Read and parse data from the starting address. Read 32 bits at a time.

After completing packet parsing, clear the `MEM_MONITOR_LOG_MEM_FULL_FLAG` flag bit by setting `MEM_MONITOR_CLR_LOG_MEM_FULL_FLAG` to 1.

### 18.5.3.2 Bus Access Logging 2 Configuration

Bus access logging 2 includes DMA bus access logging (external RAM monitoring). The configuration process is described below.

1.  Configure monitored address space: Set `MEM_MONITOR_LOG_MIN_REG` and `MEM_MONITOR_LOG_MAX_REG` to specify the monitored address space, which should range from `0x4200_0000` to `0x43FF_FFFF`.

2.  Configure the monitoring mode with `MEM_MONITOR_LOG_MODE`:
    *   Write monitoring (detects bus write operations)
    *   Word monitoring (detects writes of a specific word)
    *   Halfword monitoring (detects writes of a specific halfword)
    *   Byte monitoring (detects writes of a specific byte)

3.  Configure the specific values to monitor:
    *   In word monitoring mode, `MEM_MONITOR_LOG_CHECK_DATA_REG` specifies the monitored word.
```