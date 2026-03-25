

```markdown
not. Therefore, these two registers will retain the PC and SP values at the HP CPU reset.

## 20.5.3 CPU/DMA Bus Access Logging Configuration

### 20.5.3.1 Bus Access Logging 1 Configuration

Bus access logging 1 includes HP CPU Bus access logging (HP SRAM and external RAM monitoring), LP CPU Bus access logging (HP SRAM monitoring), and DMA Bus access logging (HP SRAM monitoring). The configuration process is described below.

1. Configure monitored address space: set `MEM_MONITOR_LOG_MIN_REG` and `MEM_MONITOR_LOG_MAX_REG` to specify monitored address space. For HP CPU, the monitored address space should be in the address range of HP SRAM (`0x4080_0000 ~ 0x4085_FFFF`) or external RAM (`0x4200_0000 ~ 0x43FF_FFFF`). For LP CPU or DMA, the monitored address space should be in the address range of HP SRAM (`0x4080_0000 ~ 0x4085_FFFF`).

2. Configure the monitoring mode with `MEM_MONITOR_LOG_MODE`:
    * Write monitoring (detects bus write operations)
    * Word monitoring (detects writes of a specific word)
    * Halfword monitoring (detects writes of a specific halfword)
    * Byte monitoring (detects writes of a specific byte)

3. Configure the specific values to be monitored.
    * In word monitoring mode, `MEM_MONITOR_LOG_CHECK_DATA_REG` specifies the monitored word.
    * In halfword monitoring mode, `MEM_MONITOR_LOG_CHECK_DATA_REG[15:0]` specifies the monitored halfword.
    * In byte monitoring mode, `MEM_MONITOR_LOG_CHECK_DATA_REG[7:0]` specifies the monitored byte.

    * `MEM_MONITOR_LOG_DATA_MASK_REG` is used to mask the byte(s) specified in `MEM_MONITOR_LOG_CHECK_DATA_REG`. A masked byte can be any value. For example, in word monitoring, if `MEM_MONITOR_LOG_CHECK_DATA_REG` is configured to `0x01020304` and `MEM_MONITOR_LOG_DATA_MASK_REG` is configured to `0x1`, then any writes of the data matching the `0x010203XX` pattern by the bus will be recorded.

4. Configure the storage space for recorded data.
    * `MEM_MONITOR_LOG_MEM_START_REG` and `MEM_MONITOR_LOG_MEM_END_REG` specify the storage space for recorded data. The storage space must be in the range of `0x4080_0000 ~ 0x4085_FFFF`.
    * Set `MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG` to update the value in `MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG` to `MEM_MONITOR_LOG_MEM_START_REG`.
    * Configure the permission of the Debug Assistant module to access the HP SRAM. The Debug Assistant module can only access HP SRAM when the access permission is enabled. For more information, please refer to Chapter 18 Permission Control (PMS).

5. Configure the writing mode for the recorded data for loop mode or non-loop mode.
```