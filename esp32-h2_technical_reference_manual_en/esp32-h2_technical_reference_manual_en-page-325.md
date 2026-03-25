

```markdown
## Register 7.57. PCR_MEM_MONITOR_CONF_REG (0x00F0)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                |                                                                             |
| ... |                                |                                                                             |
| 2   | POR_MEM_MONITOR_READY          | Represents whether or not Memory Access Monitor is released from reset.      |
| 1   | POR_MEM_MONITOR_RST_EN         | Configures whether or not to reset Memory Access Monitor.                   |
| 0   | PCR_MEM_MONITOR_CLK_EN         | Configures whether or not to enable the clock of Memory Access Monitor.      |

PCR_MEM_MONITOR_CLK_EN  
Configures whether or not to enable the clock of Memory Access Monitor.  
O: Not enable  
1: Enable  
(R/W)

PCR_MEM_MONITOR_RST_EN  
Configures whether or not to reset Memory Access Monitor.  
O: Not reset  
1: Reset  
(R/W)

PCR_MEM_MONITOR_READY  
Represents whether or not Memory Access Monitor is released from reset.  
O: Not released  
1: Released  
(RO)


## Register 7.58. PCR_TRACE_CONF_REG (0x00F8)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                |                                                                             |
| ... |                                |                                                                             |
| 2   | POR_TRACE_RST_EN               | Configures whether or not to reset RISC-V Trace Encoder.                    |
| 1   | POR_TRACE_CLK_EN               | Configures whether or not to enable the clock of RISC-V Trace Encoder.      |
| 0   |                                |                                                                             |

PCR_TRACE_CLK_EN  
Configures whether or not to enable the clock of RISC-V Trace Encoder.  
O: Not enable  
1: Enable  
(R/W)

PCR_TRACE_RST_EN  
Configures whether or not to reset RISC-V Trace Encoder.  
O: Not reset  
1: Reset  
(R/W)
```