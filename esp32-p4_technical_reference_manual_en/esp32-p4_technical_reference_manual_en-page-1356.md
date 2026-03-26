

# 21.7.2 DMA Bus Logging Configuration Registers

Register 21.13. L2_MEM_MONITOR_LOG_SETTING_REG (0x0000)

```
31                                 5   4   3   2   1   0
+-------------------------------------------------------------------------------------------------+
| RESERVED | L2_MEM_MONITOR_LOG_MEM_LOOP_ENABLE | L2_MEM_MONITOR_LOG_MODE |
+-------------------------------------------------------------------------------------------------+
Reset
```

## L2_MEM_MONITOR_LOG_MODE Configures monitoring modes.

bit[0]: Configures write monitoring.  
 0: Disable  
 1: Enable  

bit[1]: Configures word monitoring.  
 0: Disable  
 1: Enable  

bit[2]: Configures halfword monitoring.  
 0: Disable  
 1: Enable  

bit[3]: Configures byte monitoring.  
 0: Disable  
 1: Enable  
(R/W)

## L2_MEM_MONITOR_LOG_MEM_LOOP_ENABLE Configures the writing mode for recorded data.

1: Loop mode  
0: Non-loop mode  
(R/W)