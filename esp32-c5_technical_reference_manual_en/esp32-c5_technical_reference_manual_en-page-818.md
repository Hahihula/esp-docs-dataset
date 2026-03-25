

```markdown
Chapter 20 Debug Assistant
GoBack

1. Configure monitored address space: Configure `MEM_MONITOR_LOG_MIN_REG` and `MEM_MONITOR_LOG_MAX_REG` to specify monitored address space. The monitored address space should range from `0x4200_0000` to `0x43FF_FFFF`.

2. Configure the monitoring mode with `MEM_MONITOR_LOG_MODE`:
    - Write monitoring (detects bus write operations)
    - Word monitoring (detects writes of a specific word)
    - Halfword monitoring (detects writes of a specific halfword)
    - Byte monitoring (detects writes of a specific byte)

3. Configure the specific values to be monitored.
    - In word monitoring mode, `MEM_MONITOR_LOG_CHECK_DATA_REG` specifies the monitored word.
    - In halfword monitoring mode, `MEM_MONITOR_LOG_CHECK_DATA_REG[15:0]` specifies the monitored halfword.
    - In byte monitoring mode, `MEM_MONITOR_LOG_CHECK_DATA_REG[7:0]` specifies the monitored byte.

    - `MEM_MONITOR_LOG_DATA_MASK_REG` is used to mask the byte specified in `MEM_MONITOR_LOG_CHECK_DATA_REG`. A masked byte can be any value. For example, in word monitoring, if `MEM_MONITOR_LOG_CHECK_DATA_REG` is configured to `0x01020304` and `MEM_MONITOR_LOG_DATA_MASK_REG` is configured to `0x1`, then any writes of the data matching the `0x010203XX` pattern by the bus will be recorded.

4. Configure the storage space for recorded data.
    - `MEM_MONITOR_LOG_MEM_START_REG` and `MEM_MONITOR_LOG_MEM_END_REG` specify the storage space for recorded data. The storage space must be in the range of `0x4080_0000 ~ 0x4085_FFFF`.
    - Set `MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG` to update the value in `MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG` to `MEM_MONITOR_LOG_MEM_START_REG`.

    Configure the permission for the Debug Assistant module to access the HP SRAM. Only when the access permission is enabled can the Debug Assistant module access the HP SRAM. For more information, please refer to Chapter 18 Permission Control (PMS).

5. Configure the writing mode for the recorded data in loop mode or non-loop mode.
    - In loop mode, writing to the specified address space is performed in loops. When writing reaches the end address, it will return to the starting address and continue, overwriting the previously recorded data. Set `MEM_MONITOR_LOG_MEM_LOOP_ENABLE` to enable loop mode.
    - In non-loop mode, when writing reaches the end address, it will stop at the end address and dump the remaining data, not overwriting the previously recorded data. Clear `MEM_MONITOR_LOG_MEM_LOOP_ENABLE` to enable non-loop mode.
        - See examples in Section 20.5.3.1 > step 5.

6. Configure `MEM_MONITOR_LOG_DMA_O_ENA` to enable DMA_O channel groups bus access logging.
```