

```markdown
Chapter 17 Debug Assistant (ASSIST_DEBUG, MEM_MONITOR)
GoBack

17.4.2 PC Logging Configuration

Configure ASSIST_DEBUG_CORE_O_RCD_PDEBUGEN to 1 to enable CPU to update PC signals to the Debug Assistant module. If ASSIST_DEBUG_CORE_O_RCD_RECORDEN is also configured to 1, ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG will record the CPU’s PC signal and ASSIST_DEBUG_CORE_O_RCD_PDEBUGSP_REG will record the SP value. Otherwise, the two registers keep the original values.

When the CPU resets, ASSIST_DEBUG_CORE_O_RCD_EN_REG will reset, while ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG and ASSIST_DEBUG_CORE_O_RCD_PDEBUGSP_REG will not. Therefore, the two registers will keep the PC value and SP value at the CPU reset.

17.4.3 CPU/DMA Bus Access Logging Configuration

The configuration process for CPU/DMA bus access logging is described below.

1. Configure the monitored address space.
   - Configure MEM_MONITOR_LOG_MIN_REG and MEM_MONITOR_LOG_MAX_REG to specify the monitored address space.

2. Configure the monitoring mode with MEM_MONITOR_LOG_MODE:
   - write monitoring (whether the bus has write operations)
   - word monitoring (whether the bus writes a specific word)
   - halfword monitoring (whether the bus writes a specific halfword)
   - byte monitoring (whether the bus writes a specific byte)

3. Configure the specific values to be monitored.
   - In word monitoring mode, MEM_MONITOR_LOG_CHECK_DATA_REG specifies the monitored word.
   - In halfword monitoring mode, MEM_MONITOR_LOG_CHECK_DATA_REG[15:0] specifies the monitored halfword.
   - In byte monitoring mode, MEM_MONITOR_LOG_CHECK_DATA_REG[7:0] specifies the monitored byte.
   - MEM_MONITOR_LOG_DATA_MASK_REG is used to mask the byte specified in MEM_MONITOR_LOG_CHECK_DATA_REG. A masked byte can be any value. For example, in word monitoring, if MEM_MONITOR_LOG_CHECK_DATA_REG is configured to 0x01020304 and MEM_MONITOR_LOG_DATA_MASK_REG is configured to 0x1, then any writes of the data matching the 0x010203XX pattern by the bus will be recorded.

4. Configure where to store the recorded data.
   - MEM_MONITOR_LOG_MEM_START_REG and MEM_MONITOR_LOG_MEM_END_REG specify where to store the recorded data. The storage space must be in the range of 0x4080_0000 – 0x4084_FFFF.
   - Set MEM_MONITOR_LOG_MEM_ADDR_UPDATE_REG to update the value in MEM_MONITOR_LOG_MEM_START_REG to MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG.
```