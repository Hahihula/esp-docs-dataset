

```markdown
Chapter 17 Debug Assistant (ASSIST_DEBUG)

GoBack

Only when ASSIST_DEBUG_CORE_O_RCD_RECORDEN is 1, ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG samples the CPU's PC signals, otherwise, it keeps the original value.

The description of ASSIST_DEBUG_CORE_O_RCD_EN_REG and ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG can be found in section 17:18 and 17:19.

When the CPU resets, ASSIST_DEBUG_CORE_O_RCD_EN_REG will reset, while ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG will not. Therefore, the latter will keep the PC value at the CPU reset.

17.4.3 CPU/DMA Bus Access Logging Configuration Process

The configuration process for CPU/DMA bus access logging is described below.

1. Configure monitored address space.
   - Configure ASSIST_DEBUG_LOG_MIN_REG and ASSIST_DEBUG_LOG_MAX_REG to specify monitored address space.

2. Configure monitoring mode with ASSIST_DEBUG_LOG_MODE:
   - write monitoring (whether the bus has write operations)
   - word monitoring (whether the bus writes a specific word)
   - halfword monitoring (whether the bus writes a specific halfword)
   - byte monitoring (whether the bus writes a specific byte)

3. Configure the specific values to be monitored.
   - In word monitoring mode, ASSIST_DEBUG_LOG_DATA_O_REG specifies the monitored word.
   - In halfword monitoring mode, ASSIST_DEBUG_LOG_DATA_O_REG[15:0] specifies the monitored halfword.
   - In byte monitoring mode, ASSIST_DEBUG_LOG_DATA_O_REG[7:0] specifies the monitored byte.
   - ASSIST_DEBUG_LOG_DATA_MASK_REG is used to mask the byte specified in ASSIST_DEBUG_LOG_DATA_O_REG. A masked byte can be any value. For example, in word monitoring, ASSIST_DEBUG_LOG_DATA_O_REG is configured to 0x01020304, and ASSIST_DEBUG_LOG_DATA_MASK_REG is configured to 0x1, then bus writes with data matching to 0x010203XX pattern will be recorded.

4. Configure the storage space for recorded data.
   - ASSIST_DEBUG_LOG_MEM_START_REG and ASSIST_DEBUG_LOG_MEM_END_REG specify the storage space for recorded data. The storage space must be in the range of 0x3FCC_0000 ~ 0x3FCD_FFFF.
   - Configure the permission for the Debug Assistant module to access the internal SRAM. Only if the access permission is enabled, the Debug Assistant module is able to access the internal SRAM. For more information please refer to Chapter 14 Permission Control (PMS)).

5. Configure the writing mode for recorded data: loop mode and non-loop mode.
```