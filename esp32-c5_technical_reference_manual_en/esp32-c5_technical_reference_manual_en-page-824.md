

# 20.7 Registers

The addresses of bus logging configuration registers in Section 20.7.1 are relative to the `TCM_MEM_MONITOR` base address and the `PSRAM_MEM_MONITOR`. The addresses of other registers in Section 20.7.2 are relative to the `BUS_MONITOR` base address. All base addresses are provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## 20.7.1 Bus Logging Configuration Registers

Register 20.1. MEM_MONITOR_LOG_SETTING_REG (0x0000)

```
MEM_MONITOR_LOG_DMA_1_ENABLE
MEM_MONITOR_LOG_DMA_O_ENABLE
MEM_MONITOR_LOG_CORE_ENA
(reserved)
MEM_MONITOR_LOG_MEM_LOOP_ENABLE
MEM_MONITOR_LOG_MODE
```

| Bit Range | Description |
|-----------|-------------|
| 31        |             |
| 24-23     |             |
| 16-15     |             |
| 8         |             |
| 7         |             |
| 5         |             |
| 4         |             |
| 3         |             |
| 0         | Reset       |

### MEM_MONITOR_LOG_MODE Configures monitoring modes.
1: Enable write monitoring
2: Enable word monitoring
4: Enable halfword monitoring
8: Enable byte monitoring.
Other values: Invalid (R/W)

### MEM_MONITOR_LOG_MEM_LOOP_ENABLE Configures the writing mode for recorded data.
0: Non-loop mode
1: Loop mode (R/W)

### MEM_MONITOR_LOG_CORE_ENA Configures whether to enable HP CPU bus access logging.
0: Disable
1: Enable
Other values: Invalid (R/W)

Continued on the next page...