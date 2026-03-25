

```markdown
Chapter 18 Debug Assistant

GoBack

18.5.3 CPU/DMA Bus Access Logging Configuration

18.5.3.1 Bus Access Logging 1 Configuration

Bus access logging 1 includes HP CPU bus access logging (HP SRAM and external RAM monitoring) and DMA bus access logging (HP SRAM monitoring). The configuration process is described below.

1. Configure the monitored address space: set MEM_MONITOR_LOG_MIN_REG and MEM_MONITOR_LOG_MAX_REG to specify the monitored address space. For HP CPU, the monitored address space should be in the range of HP SRAM (0x4080_0000 ~ 0x4084_FFFF) or external RAM (0x4200_0000 ~ 0x43FF_FFFF). For DMA, the monitored address space should be in the range of HP SRAM (0x4080_0000 ~ 0x4084_FFFF).

2. Configure the monitoring mode with MEM_MONITOR_LOG_MODE:
    * Write monitoring (detects bus write operations)
    * Word monitoring (detects writes of a specific word)
    * Halfword monitoring (detects writes of a specific halfword)
    * Byte monitoring (detects writes of a specific byte)

3. Configure the specific values to monitor:
    * In word monitoring mode, MEM_MONITOR_LOG_CHECK_DATA_REG specifies the monitored word.
    * In halfword monitoring mode, MEM_MONITOR_LOG_CHECK_DATA_REG[15:0] specifies the monitored halfword.
    * In byte monitoring mode, MEM_MONITOR_LOG_CHECK_DATA_REG[7:0] specifies the monitored byte.
    * MEM_MONITOR_LOG_DATA_MASK_REG masks the byte(s) specified in MEM_MONITOR_LOG_CHECK_DATA_REG. A masked byte can be any value. For example, in word monitoring, if MEM_MONITOR_LOG_CHECK_DATA_REG is set to 0x01020304 and MEM_MONITOR_LOG_DATA_MASK_REG is set to 0x1, then any writes matching the 0x010203XX pattern will be recorded.

4. Configure the storage space for recorded data:
    * MEM_MONITOR_LOG_MEM_START_REG and MEM_MONITOR_LOG_MEM_END_REG specify the storage space for recorded data. The storage space must be in the range of 0x4080_0000 ~ 0x4084_FFFF.
    * Set MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG to update the value in MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG to MEM_MONITOR_LOG_MEM_START_REG.
    * Configure the Debug Assistant module’s permission to access HP SRAM. The Debug Assistant module can access HP SRAM only when the access permission is enabled. For more information, refer to Chapter 16 Permission Control (PMS).

5. Configure the writing mode for recorded data for loop mode or non-loop mode:
    * In loop mode, writing to the specified address space occurs in loops. When writing reaches the end address, it returns to the starting address and continues, overwriting previously recorded data. Set MEM_MONITOR_LOG_MEM_LOOP_ENABLE to 1 to enable loop mode.
```