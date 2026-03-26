

```markdown
- If yes and the loop mode is enabled, the address space is
SPM_MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG ~
SPM_MEM_MONITOR_LOG_MEM_END_REG and SPM_MEM_MONITOR_LOG_MEM_START_REG ~
SPM_MEM_MONITOR_LOG_MEM_CURRENT_ADDR_REG - 4.
- If yes and loop mode is not enabled, the address space is
SPM_MEM_MONITOR_LOG_MEM_START_REG ~ SPM_MEM_MONITOR_LOG_MEM_END_REG.

• Read and parse data from the starting address. Read 32 bits each time.

After packet parsing is completed, clear the SPM_MEM_MONITOR_LOG_MEM_FULL_FLAG bit by setting
SPM_MEM_MONITOR_CLR_LOG_MEM_FULL_FLAG.
```

## 21.5.3.2 DMA Bus Access Logging Configuration

The Debug Assistant module supports a total of four DMA bus channel groups, DMA_0, DMA_1, DMA_2, and DMA_3 channel groups. DMA_0 and DMA_1 channel groups are reserved and cannot be used. The DMA bus for the DMA_2 channel group is the bus on which the AXI matrix accesses the HP L2MEM. The DMA bus for the DMA_3 channel group is the bus on which the AHB matrix accesses the HP L2MEM. For more information, see Chapter 7 System and Memory > Section 7.3.2. The configuration process for DMA bus access logging (L2MEM Monitor) is described below.

1. Configure monitored address space.
   • Configure L2_MEM_MONITOR_LOG_MIN_REG and L2_MEM_MONITOR_LOG_MAX_REG to specify monitored address space. The monitored address space should range from 0x4FF0_0000 to 0x4FFB_FFFF or from 0x8FF0_0000 to 0x8FFB_FFFF.

2. Configure the monitoring mode with L2_MEM_MONITOR_LOG_MODE:
   • Write monitoring (whether the bus has write operations)
   • Word monitoring (whether the bus writes a specific word)
   • Halfword monitoring (whether the bus writes a specific halfword)
   • Byte monitoring (whether the bus writes a specific byte)

3. Configure the specific values to be monitored.
   • In word monitoring mode, L2_MEM_MONITOR_LOG_CHECK_DATA_REG specifies the monitored word.
   • In halfword monitoring mode, L2_MEM_MONITOR_LOG_CHECK_DATA_REG[15:0] specifies the monitored halfword.
   • In byte monitoring mode, L2_MEM_MONITOR_LOG_CHECK_DATA_REG[7:0] specifies the monitored byte.
   • L2_MEM_MONITOR_LOG_DATA_MASK_REG is used to mask the byte specified in L2_MEM_MONITOR_LOG_CHECK_DATA_REG. A masked byte can be any value. For example, in word monitoring, if L2_MEM_MONITOR_LOG_CHECK_DATA_REG is configured to 0x01020304 and L2_MEM_MONITOR_LOG_DATA_MASK_REG is configured to 0x1, then any writes of the data matching the 0x010203XX pattern by the bus will be recorded.

4. Configure the storage space for recorded data.
```