

```markdown
Chapter 21 Debug Assistant

GoBack

* If the interrupt is triggered by HP CPUO region monitoring, read `ASSIST_DEBUG_CORE_O_AREA_PC_REG` for the HP CPUO PC value, and `ASSIST_DEBUG_CORE_O_AREA_SP_REG` for the HP CPUO SP.
* If the interrupt is triggered by SP monitoring, read `ASSIST_DEBUG_CORE_O_SP_PC_REG` for the HP CPUO PC value.
* Write 1 to the corresponding bits of `ASSIST_DEBUG_CORE_O_INTR_RAW_REG` and `ASSIST_DEBUG_CORE_1_INTR_CLR_REG` to clear the interrupts.

21.5.2 PC Logging Configuration

Configure `ASSIST_DEBUG_CORE_O_RCD_PDEBUGEN` to 1 to enable HP CPUO to update the PC signals to the Debug Assistant module. If `ASSIST_DEBUG_CORE_O_RCD_RECORDEN` is also configured to 1, `ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG` will record the HP CPUO's PC signal and `ASSIST_DEBUG_CORE_O_RCD_PDEBUGSP_REG` will record the HP CPUO SP value. Otherwise, the two registers keep the original values.

When the HP CPUO resets, `ASSIST_DEBUG_CORE_O_RCD_EN_REG` will reset, while `ASSIST_DEBUG_CORE_O_RCD_PDEBUGPC_REG` and `ASSIST_DEBUG_CORE_O_RCD_PDEBUGSP_REG` will not. Therefore, the two registers will keep the PC value and SP value at the HP CPUO reset.

This is also the case for HP CPU1.

21.5.3 CPU/DMA Bus Access Logging Configuration

21.5.3.1 HP CPUO/1 Bus Access Logging Configuration

The configuration process for HP CPUO/1 bus access logging (SPM Monitor) is described below.

1. Configure monitored address space.
    * Configure `SPM_MEM_MONITOR_LOG_MIN_REG` and `SPM_MEM_MONITOR_LOG_MAX_REG` to specify monitored address space. The monitored address space should range from 0x3010_0000 to 0x3010_1FFF.

2. Configure the monitoring mode with `SPM_MEM_MONITOR_LOG_MODE`:
    * Write monitoring (whether the bus has write operations)
    * Word monitoring (whether the bus writes a specific word)
    * Halfword monitoring (whether the bus writes a specific halfword)
    * Byte monitoring (whether the bus writes a specific byte)

3. Configure the specific values to be monitored.
    * In word monitoring mode, `SPM_MEM_MONITOR_LOG_CHECK_DATA_REG` specifies the monitored word.
    * In halfword monitoring mode, `SPM_MEM_MONITOR_LOG_CHECK_DATA_REG[15:0]` specifies the monitored halfword.
    * In byte monitoring mode, `SPM_MEM_MONITOR_LOG_CHECK_DATA_REG[7:0]` specifies the monitored byte.

Espressif Systems
```